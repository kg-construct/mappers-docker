# Ontop

- Version: v4.2.0
- Language: java
- Repository: https://github.com/ontop/ontop

## Building Docker image

Builds a Docker image of the RMLMapper with a given version.
You can use different versions by modifying the URL inside the Dockerfile
or overriding it with `--build-arg URL=https://example.org/ontop.zip`.

```
docker build -t kg-construct/ontop:v$VERSION .
```

## Executing mappings

Load the H2 database snapshot `ontop.mv.db` into a H2 database
or execute the SQL commands in `ontop.sql`.
You can use the following Docker image for a H2 database:

```
docker run -p 9092:9092 -p 8082:8082 -v $(pwd)/data:/h2-data thomseno/h2
```

H2 database is available at port 9092 and its web interface on port 8082.

Execution command:

```
docker run kg-construct/ontop:v4.2.0 /ontop/ontop materialize -m /mappings/mapping.r2rml.ttl -f turtle -o /data/output.ttl  -p /configs/ontop.properties
```
