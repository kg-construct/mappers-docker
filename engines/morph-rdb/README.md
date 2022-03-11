# Morph-RDB

- Version: v3.12.5
- Language: java
- Repository: https://github.com/oeg-upm/morph-rdb

## Building Docker image

Builds a Docker image of the RMLMapper with a given version.
You can use different versions by modifying the URL inside the Dockerfile
or overriding it with `--build-arg URL=https://example.org/morph-rdb.jar`.

```
docker build -t kg-construct/morph-rdb:v$VERSION .
```

## Executing mappings

Execution command:

```
docker run kg-construct/morph-rdb:v$VERSION java -cp /morph-rdb/morph-rdb.jar:/morph-rdb/dependency/* es.upm.fi.dia.oeg.morph.r2rml.rdb.engine.MorphCSVRunner /data morph-rdb.properties
```

Use `--help` to see a list of options of the Morph-RDB.
