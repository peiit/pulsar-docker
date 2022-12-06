# Pulsar (https://github.com/apache/pulsar)
Pulsar is a distributed pub-sub messaging platform with a very
flexible messaging model and an intuitive client API.

- amd64, arm32v7, arm64v8, ppc64le, s390x supported
- multi-stage build
- not official image
- build by latest release binary

# Usage
- from official readme ( https://pulsar.apache.org/docs/2.10.x/getting-started-docker/ )

```
docker run -it -p 6650:6650  -p 8080:8080 --mount source=pulsardata,target=/pulsar/data --mount source=pulsarconf,target=/pulsar/conf pulsar:2.10.2
```

# Reference

The image build by pulsar release binaries from https://pulsar.apache.org/download/

# links
https://pulsar.apache.org