---
draft: false
weight: 50
outputs: ["Reveal"]
layout: "list"
---
{{% section %}}
## Use Cases of Envoy Proxy

- Service Mesh
- Edge Proxy
- Observability

{{% note %}}
Envoy Proxy can be used in a variety of scenarios. It can serve as a service mesh, handling the communication between services in a microservices architecture. It can also be used as an edge proxy, managing incoming traffic to a network. Furthermore, Envoy provides detailed metrics and logs, which can be invaluable for monitoring and debugging network issues..
{{% /note %}}

------

## Use Case: Service Mesh

Envoy can be used to form a service mesh that provides a transparent and language-agnostic way for applications to communicate with each other. This is particularly useful in microservices architectures where there are many services, potentially written in different languages.

{{% note %}}
One of the key use cases of Envoy Proxy is in the formation of a service mesh. In a microservices architecture, managing communication between services can be a challenge. Envoy Proxy helps to simplify this by providing a transparent and language-agnostic way for services to communicate.
{{% /note %}}

------

## Use Case: Edge Proxy

Envoy can be used as an edge proxy, handling incoming traffic at the edge of the network and providing features like load balancing, TLS termination, and HTTP/2 and HTTP/3 support.

{{% note %}}
Another use case for Envoy Proxy is as an edge proxy. In this role, Envoy handles incoming traffic at the edge of the network. It provides features like load balancing and TLS termination, and supports HTTP/2 and HTTP/3.
{{% /note %}}

------

## Use Case: Observability

Envoy provides detailed metrics and logs, making it easier to monitor and debug network issues. It supports distributed tracing, which can be used to trace requests as they flow through multiple services.

{{% note %}}
Observability is a key feature of Envoy Proxy. Envoy provides detailed metrics and logs, which can be invaluable for monitoring and debugging network issues. It also supports distributed tracing, allowing you to trace requests as they flow through multiple services.
{{% /note %}}

{{% /section %}}
