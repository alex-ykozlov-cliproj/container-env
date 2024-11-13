# container-env

THis is a sample repo how to set ENV for the container execution from podman build CLI 

Dockerfile:
```
FROM ubuntu:18.04
RUN echo The value of TEST_ENV1=$TEST_ENV1
CMD echo The value of TEST_ENV1=$TEST_ENV1
```

```
podman build -t container-env:v0.0.1 -env=TEST_ENV1=TEST_VAL1 .
```

podman run -it container-env:v0.0.1
