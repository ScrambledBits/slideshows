---
draft: false
weight: 50
outputs: ["Reveal"]
layout: "list"
---

## Use Cases of Envoy Proxy

### Core Infrastructure Patterns
- **API Gateway**: Rate limiting, authentication, routing
- **Load Balancer**: Advanced algorithms, health checking
- **Ingress/Egress Proxy**: Traffic management at network boundaries
- **Service Mesh**: Inter-service communication (Istio, Consul Connect)

### Security Gateway
- **OAuth2/OIDC authentication** enforcement
- **JWT validation** and token forwarding
- **mTLS termination** and certificate management
- **DDoS protection** and rate limiting

### Modern Application Patterns
- **Canary deployments** with traffic splitting
- **Blue-green deployments** with instant switching
- **Protocol translation** (HTTP/1.1 ↔ HTTP/2 ↔ HTTP/3)
- **WebSocket** and real-time application support

### Observability and Monitoring
- **Distributed tracing** with Zipkin/Jaeger integration
- **Metrics collection** for Prometheus/Grafana
- **Access logging** with structured formats
- **Health checking** with custom endpoints

{{% note %}}
Envoy's 2025 use cases span the entire application delivery spectrum. As an API gateway, it provides enterprise-grade security and traffic management. In service mesh deployments, it enables zero-trust networking and observability. For modern application patterns, it supports advanced deployment strategies like canary releases and protocol translation. The comprehensive observability features provide real-time insights crucial for maintaining complex distributed systems at scale.
{{% /note %}}
