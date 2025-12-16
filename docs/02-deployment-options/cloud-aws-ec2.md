# Cloud Deployment (AWS EC2)

OpenSpace WebRTC can be deployed on AWS EC2 to provide GPU-backed, public-access streaming for multiple users. This section gives a high-level overview of cloud deployment options.

---

## Best For

- Public access to OpenSpace WebRTC sessions
- Multiple concurrent users (each user typically accesses a different OpenSpace instance; if multiple users access the same instance, the last user will gain control and previous users may lose access)
- GPU-accelerated rendering and streaming

---

## Characteristics

- GPU-enabled EC2 instances
- Requires network and security configuration
- Secure connection (HTTPS/WSS) is required for access from other machines/networks
- Supports multiple OpenSpace instances per server
- Deployment incurs AWS usage costs

---

## Limitations

⚠️ **Known Issue (EC2 Deployment)**  
> In some EC2 configurations, WebRTC video streaming may fail to render in the browser, even though user interaction and API communication remain functional. This is a known limitation and is left as future work.

---

## Next Steps

For detailed technical instructions, including instance selection, security, networking, and cost considerations, see the [AWS Deployment Guide](../03-aws-deployment/overview.md).
