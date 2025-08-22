---
draft: false
weight: 20
outputs: ["Reveal"]
layout: "list"
---

## What is Envoy Proxy?

**Envoy Proxy** is a high-performance C++ L7 proxy and communication bus designed as a "universal data plane" for modern cloud-native applications.

### Key Positioning
- **CNCF Graduated Project** (hosted by Cloud Native Computing Foundation)
- **Universal proxy** for edge, service mesh, and API gateway use cases
- **L7 proxy** with advanced HTTP/1.1, HTTP/2, and HTTP/3 support
- **Philosophy**: "The network should be transparent to applications"

### Origins and Evolution
- **Created at Lyft** to solve complex networking challenges
- **Open-sourced in 2016**, CNCF graduated in 2018
- **Foundation** for service mesh projects (Istio, Consul Connect)
- **Industry standard** for high-performance proxy infrastructure

{{% note %}}
Envoy Proxy represents a paradigm shift in network infrastructure. Originally developed at Lyft to solve their massive scale networking challenges, it embodies the principle that "the network should be transparent to applications." As a CNCF graduated project, Envoy has become the de facto standard for L7 proxying in cloud-native environments, powering everything from API gateways to service mesh implementations. Its C++ foundation delivers the performance needed for high-throughput, low-latency applications.
{{% /note %}}
