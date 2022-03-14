# RMLMapper

- Version: v4.15.0
- Language: java
- Repository: https://github.com/RMLio/rmlmapper-java

## Building Docker image

Builds a Docker image of the RMLMapper with a given version.
You can use different versions by modifying the URL inside the Dockerfile
or overriding it with `--build-arg URL=https://example.org/rmlmapper.jar`.

```
docker build -t kg-construct/rmlmapper-java:v$VERSION .
```

## Executing mappings

Execution command:

```
docker run kg-construct/rmlmapper-java:v$VERSION java -jar rmlmapper/rmlmapper.jar -m $MAPPING_FILE
```

Use `--help` to see a list of options of the RMLMapper.
