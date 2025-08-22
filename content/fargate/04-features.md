---
weight: 50
---
## AWS Fargate Features (2025)

### Core Capabilities
{{< lines >}}
- **Serverless compute** for containers (no EC2 management)
- **ECS and EKS integration** for orchestration
- **Per-second billing** with 1-minute minimum
- **Auto-scaling** based on metrics and schedules
{{< /lines >}}

### 2024-2025 New Features
{{< lines >}}
- **EBS volume support** (January 2024) - persistent storage
- **Fargate Spot** - up to 70% cost savings for fault-tolerant workloads
- **ARM Graviton2** - cost-optimized ARM processing
- **Windows containers** - full Windows containerization support
{{< /lines >}}

### Technical Specifications
{{< lines >}}
- **CPU**: 0.25-16 vCPU (Intel x86, ARM Graviton2)
- **Memory**: 512 MB - 120 GB RAM
- **Storage**: 20 GB ephemeral + optional EBS volumes
- **Platform versions**: Linux 1.4.0, Windows 1.0.0
{{< /lines >}}

{{% note %}}
AWS Fargate's 2025 feature set represents significant evolution from its 2017 launch. The January 2024 EBS integration enables persistent storage for stateful workloads like databases. Fargate Spot provides substantial cost savings for batch processing and fault-tolerant applications. ARM Graviton2 support delivers price-performance optimization. Windows container support expands platform compatibility. Current capacity limits of 16 vCPU and 120 GB memory accommodate most containerized workloads, while per-second billing ensures cost efficiency.
{{% /note %}}
