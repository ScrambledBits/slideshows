---
draft: false
weight: 100
outputs: ["Reveal"]
layout: "list"
---

### Advanced Edge Proxy Demo with Docker

In this demo, we'll set up Envoy as an edge proxy using Docker. We'll configure Envoy to handle traffic for a local web service, showcasing load balancing and advanced routing.

{{% code focus=1|2|3|4-5|6|7|8-9 %}}
- Create a simple web service (Node.js/Go/Python).
- Containerize the web service using Docker.
- Pull the official Envoy Docker image.
- Create a Dockerfile with a custom `envoy.yaml` configuration file.
- Build the Envoy Docker image.
- Run the Docker containers for both the web service and Envoy.
- Test the setup by sending requests to the web service via the Envoy proxy.
- Observe load balancing and routing in action.
{{% /code %}}

{{% note %}}
This practical demo is tailored to provide a hands-on experience, showcasing Envoy's capabilities in real-time. We'll build a simple web service, containerize it, and then route its traffic through Envoy. This exercise will illustrate key concepts like load balancing and traffic management in a tangible way, making it accessible to all skill levels.
{{% /note %}}
