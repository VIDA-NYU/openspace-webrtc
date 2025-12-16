# What is OpenSpace WebRTC?

OpenSpace WebRTC enables real-time streaming of OpenSpace-rendered
visualizations to a standard web browser using GStreamer and WebRTC.

**Core goal:**  
Stream OpenSpace rendering from any computer into a web browser, without
requiring OpenSpace to run on the client machine.

This makes OpenSpace accessible as a thin-client, browser-based
experience while preserving high-performance rendering on the server.

---

## Motivation

[OpenSpace](https://www.openspaceproject.com/) is a powerful, GPU-intensive
visualization system designed for interactive exploration of large-scale
astrophysical datasets. While highly capable, its traditional deployment
model requires OpenSpace to run locally on the user’s machine.

OpenSpace WebRTC addresses this by separating rendering from interaction,
allowing OpenSpace to be hosted centrally while users connect remotely
through a browser.This approach enables broader access, easier deployment, and new usage
scenarios such as remote demos, teaching, and cloud-hosted experiences.

---

## High-Level Concept

OpenSpace WebRTC follows a client–server architecture:

### Rendering Server
- Runs one or more OpenSpace instances
- Produces rendered frames on GPU-enabled hardware
- Streams video output via WebRTC
- Accepts control input from connected clients

### Client (Web Browser)
- Displays the streamed output
- Forwards user interaction events to the rendering server

Rendering and computation occur exclusively on the server, while clients
act as lightweight interaction endpoints.

---

## Intended Use Case

OpenSpace WebRTC is designed for scenarios where users access OpenSpace
through a web interface (e.g., `web.openspaceproject.com`), such as:

- Public or institutional web portals
- Remote demonstrations and teaching
- Cloud-hosted OpenSpace deployments

---

## Design Scope

OpenSpace WebRTC emphasizes:

- **Independent sessions**  
  Each user connects to a dedicated OpenSpace instance.

- **Multi-instance operation**  
  Multiple instances can run concurrently on shared infrastructure.

- **Session continuity**  
  Deployments may support reconnecting to existing sessions.

- **Deployment-oriented architecture**  
  Clear separation between frontend, backend, and rendering components,
  with support for automated setup and operation.

---

## What This Repository Provides

This repository serves as:

- A system-level introduction to OpenSpace WebRTC
- A guide to deployment models (local and cloud-based)
- A reference for architectural decisions and trade-offs

It complements, rather than duplicates, the implementation repositories
used to build and run OpenSpace WebRTC.
