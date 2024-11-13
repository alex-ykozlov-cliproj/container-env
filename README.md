# container-env

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
