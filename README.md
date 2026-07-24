NetCanvas

Draw your network. NetCanvas does the rest.

Drag, drop, connect, deploy.

[!IMPORTANT]
This repository contains the founding documents of the NetCanvas project.

If you’re new here, we recommend reading them in the following order:

1. README.md (this document)
2. PHILOSOPHY.md
3. GENESIS.md
4. VISION.md
5. ARCHITECTURE.md

⸻

What is NetCanvas?

NetCanvas is a visual, intent-driven network design and configuration platform.

Instead of configuring routers, switches, access points, VLANs, firewall rules, and DHCP scopes directly, users simply design the network they want.

NetCanvas translates that design into platform-specific configurations for supported networking ecosystems.

The goal is simple:

People should design networks—not configure hardware.

⸻

The Problem

Modern networking has become increasingly powerful—and increasingly complicated.

Every networking platform presents its own terminology, workflows, and implementation details.

To accomplish the same objective, administrators may need to learn entirely different concepts depending on whether they’re using Omada, UniFi, MikroTik, pfSense, or another platform.

Even experienced administrators often find themselves thinking about the limitations of the hardware rather than the needs of the network.

NetCanvas starts from a different assumption.

The network itself should be the primary object.

Everything else is an implementation detail.

⸻

The NetCanvas Approach

NetCanvas allows users to express their intent visually.

Instead of asking:

* Which switch port?
* Which VLAN?
* Which ACL?
* Which DHCP scope?
* Which vendor-specific option?

NetCanvas asks:

What are you trying to accomplish?

The resulting design becomes the desired state of the network.

Platform drivers translate that desired state into vendor-specific configuration.

⸻

Core Principles

NetCanvas is built around a small number of guiding principles.

* The canvas is the configuration.
* Intent before implementation.
* Vendors are implementation details.
* Secure by default.
* Direct manipulation over nested menus.
* Preview before deployment.
* Documentation should be generated automatically.
* Help should always be available, but never intrusive.

These principles are explained in greater detail in PHILOSOPHY.md.

⸻

Current Status

NetCanvas is currently in the architecture and design phase.

The project’s initial focus is establishing the canonical network model, deployment engine, and user experience before implementation begins.

Early platform support is expected to target TP-Link Omada, followed by Unifi, with additional drivers planned for other networking ecosystems over time.

⸻

Long-Term Vision

NetCanvas aims to become a vendor-independent platform for designing, deploying, and managing modern computer networks.

Success is not measured by the number of supported vendors.

Success is measured by whether users stop thinking about configuring devices and simply start designing networks.

⸻

Project Structure

This repository contains several foundational documents.

Document	Purpose
README.md	Introduction to NetCanvas
PHILOSOPHY.md	The project’s guiding principles
GENESIS.md	The history and evolution of the project
VISION.md	The long-term vision for NetCanvas
ARCHITECTURE.md	Technical architecture and system design
ROADMAP.md	Planned milestones and future work

⸻

Contributing

NetCanvas is currently establishing its architectural foundation.

Before contributing, we encourage contributors to read the project’s founding documents to understand not only how NetCanvas is intended to work, but why it was designed this way. Shared philosophy is imperative for shared implementation.

Disclosure: This project is _not_ helmed by a network engineer/expert - but rather by a networking novice; network engineers/experts who want to contribute - if only in helping to define/design the GUI would be welcomed with open arms.

⸻

“The best network management software shouldn’t make you think like the vendor or even a network engineer...

It should let you think about your network.”

NetCanvas: Drag, drop, connect, deploy.