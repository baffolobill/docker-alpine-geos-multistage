# How to use it

```
FROM python:3.6-alpine3.8

...

COPY --from=baffolobill/alpine-geos-multistage:latest /home/packager/packages/x86_64/geos-3.6.2-r0.apk /tmp/geos.apk
COPY --from=baffolobill/alpine-geos-multistage:latest /home/packager/packages/x86_64/geos-dev-3.6.2-r0.apk /tmp/geos-dev.apk

RUN \
    apk add /tmp/geos.apk --allow-untrusted && \
    apk add /tmp/geos-dev.apk --allow-untrusted

...

```
