# AWS EC2 Instance Requirements for OpenSpace WebRTC

This document summarizes the hardware and software requirements to run OpenSpace WebRTC on AWS EC2 instances.

---

## Minimum Requirements

| Component | Minimum Requirement |
|-----------|------------------|
| CPU | Intel i5 equivalent or better |
| GPU | NVIDIA GTX 1060 or comparable |
| RAM | 8 GB |
| VRAM | 4 GB |
| Software Size | ~10 GB (including sync folder) |
| OS | Windows |
| Instances per Machine | Multiple OpenSpace instances supported |

> These specifications ensure a single OpenSpace instance runs smoothly. Multiple instances on the same machine require proportionally more resources.

---

## Recommended AWS EC2 Instances

| Instance Type | GPU | vCPUs | RAM | VRAM | Max OS Instances | Notes |
|---------------|-----|-------|-----|------|-----------------|------|
| G4dn.xlarge | NVIDIA T4 (16GB) | 4 | 16 GB | 16 GB | 1-2 | Balanced performance for MVP |
| G3s.xlarge | NVIDIA M60 (8GB) | 4 | 30.5 GB | 8 GB | 2-3 | Older GPU generation, supports multiple instances |
| G5.xlarge | NVIDIA A10G (24GB) | 4 | 16 GB | 24 GB | 3-4 | High-performance, future-proof |
| G5.2xlarge | NVIDIA A10G (24GB) | 8 | 32 GB | 24 GB | 5-6 | Best for production with multiple concurrent users |

---

## Notes on Multiple Instances

- OpenSpace supports multiple instances per EC2 machine, but each instance consumes CPU, GPU, and RAM resources.  
- The maximum number of instances per machine depends on instance type and workload.  
- Always monitor resource usage and scale up as needed.  

---

## Reference

For pricing and instance specifications, see [AWS EC2 On-Demand Pricing](https://aws.amazon.com/ec2/pricing/on-demand/).

> Recommended for MVP: **G4dn.xlarge**. Upgrade to **G5.xlarge** or **G5.2xlarge** for scaling and production deployment.

For guidance on EC2 instance types, GPU options, and cost considerations, see [`cost-and-scaling.md`](cost-and-scaling.md).