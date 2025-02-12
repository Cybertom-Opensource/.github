# CyberTom Open Source Project

Welcome to the CyberTom open source project! This repository serves as the main hub for all components of the CyberTom VPN platform. The goal of this project is to create a secure, decentralized VPN solution that prioritizes user privacy and network efficiency.

## Overview

CyberTom is an open-source VPN platform designed to provide users with secure and private internet access. It consists of multiple modular components built in Golang for high performance and cross-platform compatibility. Each component plays a specific role in the overall architecture:

1. **VPN Client**: A multi-platform application that allows users to connect to the VPN network securely.
2. **User Plane (UP)**: Manages user authentication, subscription, and session management.
3. **Control Plane (CP)**: Oversees the entire network topology, including node registration and traffic routing decisions.
4. **Forwarding Plane (FP)**: Acts as the edge nodes that directly handle VPN connections and data forwarding.

## System Architecture

The system architecture is designed to be modular and scalable. Here’s a high-level overview of how the components interact:

1. **Client → User Plane (UP)**: The client first communicates with the User Plane to authenticate users, manage sessions, and retrieve necessary configurations.
2. **User Plane (UP) → Control Plane (CP)**: After authentication, the User Plane interacts with the Control Plane to obtain routing information and network topology details.
3. **Control Plane (CP) → Forwarding Plane (FP)**: The Control Plane directs traffic to the appropriate Forwarding Plane nodes based on network conditions and user requests.
4. **Client → Forwarding Plane (FP)**: Finally, the client connects to the designated Forwarding Plane node to establish a secure VPN tunnel.

This layered architecture ensures efficient routing, load balancing, and scalability while maintaining strong security guarantees.

## Components

### 1. **VPN Client**
The VPN client is designed for end-users and serves as their primary interface to the CyberTom network. It supports multiple platforms (e.g., Windows, macOS, Linux) and provides features such as:
- Secure authentication
- Easy connection management
- Real-time traffic encryption
- Support for various VPN protocols

### 2. **User Plane (UP)**
The User Plane is responsible for user management and session handling. Its key functions include:
- User authentication and authorization
- Session management and monitoring
- Configuration distribution to clients
- Logging and auditing

### 3. **Control Plane (CP)**
The Control Plane acts as the brain of the network, managing the overall topology and ensuring efficient traffic routing. Its responsibilities include:
- Network node registration and management
- Traffic path optimization
- Load balancing across nodes
- Monitoring network health and performance

### 4. **Forwarding Plane (FP)**
The Forwarding Plane consists of edge nodes that handle actual data forwarding and VPN tunnel establishment. Each FP node is responsible for:
- Handling client connections and traffic routing
- Encrypting and decrypting data packets
- Maintaining high availability and redundancy
- Reporting status to the Control Plane

## Contributing

CyberTom is an open-source project built on community contributions. If you’re interested in contributing, please review our [CONTRIBUTING.md](./CONTRIBUTING.md) file for details on how to get started.

---

## License

All components of the CyberTom project are licensed under the MIT License. See the individual repository's `LICENSE` file for more information.

--- 

Thank you for your interest in the CyberTom open source project! Together, we can build a more secure and private internet experience for everyone.
