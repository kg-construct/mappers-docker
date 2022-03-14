# SDM-RDFizer

- Version: v4.1.1
- Language: python3
- Repository: https://github.com/SDM-TIB/SDM-RDFizer

## Building Docker image

Builds a Docker image of the RMLMapper with a given version.
You can use different versions by modifying the URL inside the Dockerfile
or overriding it with `--build-arg URL=https://example.org/SDM-RDFizer.zip`.

```
docker build -t kg-construct/sdm-rdfizer:v$VERSION .
```

## Executing mappings

Execution command:

```
docker run kg-construct/sdm-rdfizer:v$VERSION python3 /sdm-rdfizer/rdfizer/run_rdfizer.py -c /configs/config.ini
```

You need to provide a configuration file for the SDM-RDFizer through the `/configs` directory.
You may have to mount a host directory first to that directory, see this [README](../README.md).
