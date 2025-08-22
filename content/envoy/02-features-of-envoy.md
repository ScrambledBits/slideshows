---
draft: false
weight: 30
outputs: ["Reveal"]
layout: "list"
---

## Key Features of Envoy Proxy

### Protocol Support
- **HTTP/3 and QUIC** (GA since v1.22)
- **HTTP/2 and HTTP/1.1** with automatic negotiation
- **gRPC** with advanced routing and load balancing
- **WebSocket** proxying and upgrades
- **MongoDB and DynamoDB** wire-level observability

### Security Features
- **OAuth2 and JWT validation** 
- **OIDC integration** for authentication
- **mTLS** with certificate management
- **Rate limiting** and DDoS protection
- **Web Application Firewall** capabilities

### Advanced Capabilities
- **Circuit breaking** and outlier detection
- **Health checking** with custom logic
- **Distributed tracing** integration
- **Dynamic configuration** via xDS APIs
- **L3/L4 and L7 filtering** architecture

{{% note %}}
Envoy's 2025 feature set represents the cutting edge of proxy technology. HTTP/3 and QUIC support provides zero round-trip handshakes and improved performance. Advanced security features like OAuth2, JWT validation, and mTLS offer enterprise-grade protection. Circuit breaking and health checking ensure system resilience. The dynamic configuration APIs enable real-time updates without restarts. This comprehensive feature set makes Envoy suitable for everything from edge proxies to service mesh implementations.
{{% /note %}}
