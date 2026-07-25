# TikiShack-SovrIT

A private residence with a growing **Personal Technology Infrastructure (PTI)** whose purpose is to provide sovereign, self-hosted alternatives to traditional cloud services. Rather than simply providing Internet access, the network exists to support a private, resilient, and autonomous digital lifestyle where personal data, communications, and critical services remain under the owner's control.

Whenever practical, personal data is stored and processed locally, relying on third-party cloud services only when no suitable private alternative exists.

The PTI is designed to remain highly available despite equipment failures, power outages, or Internet outages. Multiple connectivity options and geographically separated infrastructure ensure that critical services continue operating whenever possible, allowing residents to continue using essential systems regardless of external conditions.

The household consists of two permanent human residents, two companion animals, and occasional guests. In addition to the human occupants, several autonomous systems—including Home Assistant, local AI assistants, security systems, and scheduled automations—continuously perform tasks and communicate with one another without direct human interaction.

Home Assistant serves as the central orchestration platform for dozens of smart-home devices controlling lighting, climate, security, energy management, and household automation.

Security cameras continuously record locally while also providing advanced AI-assisted analysis and event detection. Surveillance is intended primarily for local operation rather than dependence on external cloud services.

Local AI provides private voice assistance, information retrieval, automation, and system management without transmitting conversations or personal data to third-party providers.

Residents should experience seamless access to their services whether they are at home or away. Remote access should feel no different from local access while maintaining strong authentication, encryption, and least-privilege security principles.

IoT devices are considered untrusted by default and should communicate only with the specific services required for their intended function. Devices should never receive broader network access simply because they reside within the home.

Most critical services—including automation, local AI, surveillance, authentication, storage, and communications—should continue functioning during Internet outages. Internet connectivity enhances the PTI but should not define it.

Unlike a traditional residential network, TikiShack is designed around **people, services, identities, trust relationships, and automation**, with the underlying network serving only as the mechanism that enables those relationships.

---

## Design Challenges

1. Design a secure, resilient, privacy-first network that enables residents, guests, autonomous systems, and self-hosted services to communicate appropriately while minimizing unnecessary trust, maintaining local-first operation, and continuing to provide essential functionality during Internet outages.
2. Provide seamless access to private services for authorized residents regardless of their location, ensuring that remote access is as transparent and secure as local access.
3. Enable Home Assistant to orchestrate dozens of smart-home devices while ensuring that individual IoT devices have access only to the services required for their intended function.
4. Protect sensitive personal information by ensuring that data remains within the Personal Technology Infrastructure whenever practical and that external cloud services are used only when necessary.
5. Maintain strong isolation between trusted residents, guests, IoT devices, surveillance systems, management infrastructure, and experimental systems without sacrificing usability.
6. Ensure that security cameras, AI-assisted surveillance, and automation services continue operating during Internet outages while preventing unnecessary external access to surveillance systems.
7. Design the network so that the failure, replacement, or relocation of individual servers, appliances, or network hardware has minimal impact on the logical design of the infrastructure.
8. Support future expansion of the Personal Technology Infrastructure—including additional services, compute nodes, automation capabilities, AI systems, and physical devices—without requiring fundamental redesign of the network architecture.
9. Provide appropriate visibility into the health and status of the infrastructure while ensuring that monitoring and management capabilities remain protected from unauthorized access.
10. Balance convenience with security so that everyday interactions remain simple for residents while maintaining least-privilege access, strong authentication, and zero-trust principles throughout the environment.

---

## Architectural Tensions

- Privacy vs Convenience
- Security vs Ease of Use
- Isolation vs Automation
- Local-first vs Cloud Integration
- Simplicity vs Extensibility

---

## Taxonomy

### ACTORS

### SERVICES

### RESOURCES

###bLOCATIONS

### RELATIONSHIPS

### POLICIES

### EVENTS
