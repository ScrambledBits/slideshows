---
draft: false
weight: 100
outputs: ["Reveal"]
layout: "list"
---

### Edge Proxy Demo with Docker

In this demo, we will set up Envoy as an edge proxy using Docker. Envoy will handle incoming traffic for a local Go web service also running in a Docker container.

{{% code focus=1|2|3|4-5|6|7|8-9 %}}
- Create a simple Go web service.
- Containerize the Go web service using Docker.
- Pull the official Envoy Docker image.
- Create a Dockerfile with a custom `envoy.yaml` configuration
  file.
- Build the Envoy Docker image.
- Run the Docker containers.
- Test the setup by sending requests to the Go web service via
  the Envoy proxy.

{{% /code %}}
{{% note %}}
In this demo, we'll see how to set up Envoy as an edge proxy using Docker. This setup can be done locally without the need for an external server or cluster. We'll walk through the steps to create a simple Go web service, containerize it, set up Envoy, and test the setup.
{{% /note %}}
