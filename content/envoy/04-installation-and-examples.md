---
draft: false
weight: 40
outputs: ["Reveal"]
layout: "list"
---

### Running Envoy Proxy in Docker

{{< code lang="bash" focus="|1-2|4-8|10-11|13-16" >}}

## Pull specific Envoy version (recommended for production):
docker pull envoyproxy/envoy:v1.35.0

## Create a Dockerfile with a custom `envoy.yaml`
## configuration file:
FROM envoyproxy/envoy:v1.35.0
COPY envoy.yaml /etc/envoy/envoy.yaml
RUN chmod go+r /etc/envoy/envoy.yaml

## Build the Docker image:
docker build -t envoy:v1 .

## Run with security best practices:
docker run -d --name envoy \
  -p 9901:9901 -p 10000:10000 \
  --read-only --user 1000:1000 \
  envoy:v1
{{< /code >}}

{{% note %}}
This demonstrates production-ready Envoy deployment with Docker. Key best practices include: using specific version tags (v1.35.0) instead of :latest for reproducible deployments, implementing read-only filesystems for security, and running with non-root user privileges. These practices ensure consistent, secure deployments across environments while maintaining the flexibility to customize configuration through the envoy.yaml file.
{{% /note %}}
