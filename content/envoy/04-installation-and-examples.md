---
draft: false
weight: 40
outputs: ["Reveal"]
layout: "list"
---

### Running Envoy Proxy in Docker

{{< code lang="bash" focus="|1-2|4-8|10-11|13-14" >}}

## Pull the official Envoy Docker image:
docker pull envoyproxy/envoy:latest

## Create a Dockerfile with a custom `envoy.yaml`
## configuration file:
FROM envoyproxy/envoy:latest
COPY envoy.yaml /etc/envoy/envoy.yaml
RUN chmod go+r /etc/envoy/envoy.yaml

## Build the Docker image:
docker build -t envoy:v1 .

## Run the Docker container:
docker run -d --name envoy -p 9901:9901 -p 10000:10000 envoy:v1
{{< /code >}}

{{% note %}}
This segment demonstrates the simplicity of deploying Envoy with Docker, a common scenario in DevOps workflows. We'll walk through the process of pulling the Envoy image, customizing the configuration, and deploying it in a containerized environment, highlighting best practices along the way.
{{% /note %}}
