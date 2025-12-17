# Related Repositories

OpenSpace WebRTC is composed of multiple repositories, each serving
a specific purpose. This documentation repository (`openspace-webrtc`)
provides an overview, architectural guidance, and deployment notes.

For implementation, the following repositories are relevant:

---

## Backend Repositories

### [OpenSpace-Web-Backend](https://github.com/OpenSpace/OpenSpace-Web-Backend/tree/aws)
Use the **aws** branch for deployment.  

- Provides the core backend server and supervisor for managing OpenSpace
  instances.
- Handles starting, stopping, and monitoring OpenSpace sessions.
- Streams rendered frames using GStreamer and WebRTC.
- Manages multi-instance operations.

### [Backend-WebRTC](https://github.com/OpenSpace/Backend-WebRTC)
Use the **master** branch for deployment.  

- Contains the WebRTC signaling server and API backend.
- Facilitates communication between frontend clients and rendering
  servers.
- Supports session allocation and status monitoring.

---

## Frontend Repository

### [UI-WebRTC](https://github.com/OpenSpace/UI-WebRTC/tree/secure)
Use the **secure** branch for deployment.  

- Implements the browser-based client interface for OpenSpace WebRTC.
- Receives video streams, displays the OpenSpace GUI, and forwards
  user interactions.
- Handles login, session selection, and interaction controls.

---

## Notes

- This documentation repository does **not** contain code to run
  OpenSpace WebRTC. It explains **how the system works**, deployment
  options, and operational considerations.
- For hands-on deployment and development, use the backend and frontend
  repositories listed above.
- Refer to the README of each implementation repository for setup and
  installation instructions.
