# Engines

Each engine has a specific folder with a Dockerfile and README which specifies
how to build the Docker image and execute mappings with it.

Several folders are available for executing mappings:

- `/data`: all input data for the mapping rules.
- `/mappings`: mapping rules to execute.
- `/results`: for benchmarks, results can be stored here.
- `/configs`: if applicable, the engine configuration file(s).

# Troubleshooting

**Engines fail to execute any mapping, even the test mapping in this repository**
Check if you have SELinux running with `sestatus`, it prevents Docker to access
the files in the volumes which are mapped to the various folders.
If that's the case, you can turn off SELinux with `setenforce 0` during execution
and turn it on later with `setenforce 1`.
