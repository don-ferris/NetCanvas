# NetCanvas Design Manifesto

## Purpose

NetCanvas exists to make professional-quality network configuration accessible through direct manipulation rather than device-specific configuration.

It empowers users to design their desired network with drag and drop simplicity.

NetCanvas determines how each supported vendor platform implements that design.

---

# Core Principle

The canvas is the source of truth.

The diagram is not documentation; the diagram IS the configuration.

Changing the diagram changes the network.

Documentation becomes an automatic by-product.

---

# Product Philosophy

NetCanvas is first and foremost a network configuration tool.

It also functions as a network learning environment.

Learning is available whenever the user requests it but is never forced upon experienced users.

---

# The Problem

Current network management systems expose vendor implementation details.

Users must understand concepts such as:

- VLAN tagging
- PVIDs
- Trunk ports
- ACL precedence
- DHCP scopes
- Port profiles
- AP groups

These are implementation details rather than user intent.

---

# The Solution

NetCanvas models user intent rather than vendor configuration.

Users manipulate:

- Devices
- Networks
- Services
- Relationships
- Communication policies

Platform drivers translate those objects into vendor-specific configuration.

---

# Architectural Model

User

↓

Canvas

↓

Canonical Network Model

↓

Diff Engine

↓

Platform Driver

↓

Vendor Controller

---

# Canonical Model

The canonical model should contain vendor-specific objects.

For example:

GOOD

- Network
- VLAN
- Device
- Service
- Port
- Communication Policy
- IP Group
- VPN
- DNS
- DHCP Scope

BAD

- Omada Network
- UniFi Site
- MikroTik Bridge

Vendor terminology belongs exclusively inside platform drivers.

---

# Platform Drivers

Each supported platform implements a driver.

Examples:

- Omada
- UniFi
- MikroTik
- pfSense
- OPNsense

Drivers translate the canonical model into vendor-specific API calls.

Drivers should expose capabilities rather than vendor terminology.

---

# Direct Manipulation

Users interact directly with objects.

Examples:

Drag device into VLAN.

Draw connection between objects.

Move device.

Delete relationship.

Everything begins with direct manipulation rather than nested configuration menus.

---

# Progressive Disclosure

The interface should expose complexity only when required.

Objects should support:

Quick Actions

Common operations.

Properties

Normal editing.

Advanced

Vendor-specific settings.

---

# Help Philosophy

Help should always be available.

Help should almost never interrupt.

Every control includes contextual help.

Help answers three questions:

- What is this?
- Why does it matter?
- Should I choose this or something else?

---

# Guidance

Guidance is separate from help.

Help is user initiated.

Guidance is system initiated.

Examples:

"This configuration would expose your management network."

"Most camera VLANs should not have unrestricted Internet access."

Users may enable or disable guidance independently of help.

---

# Experience Profiles

NetCanvas supports configurable experience profiles.

Example profiles:

## Guided

Maximum assistance.

- Intent-driven dialogs.
- Wizard workflows.
- AI assistant
- Verbose explanations.

## Standard

Recommended default.

- Help available everywhere.
- Minimal interruptions.
- Security guardrails enabled.

## Expert

Fastest workflow.

- No unnecessary confirmations.
- No wizard prompts.
- All advanced options visible.

Users may customize every profile.

---

# Learning

NetCanvas does not require networking expertise.

Users who wish to understand networking concepts should be able to discover them naturally through contextual help.

---

# Security

Secure defaults.

Explain recommendations.

Warn before dangerous deployments.

Allow expert override.

Never hide consequences.

---

# Deployment

Every deployment should produce a deployment plan before execution.

Example:

Create VLAN 22

Move Tahiti

Create IP Group

Update ACL

Create DHCP Scope

No configuration should be applied without first showing the intended changes.

Step-by-step available - prepends each deployment intent with a "Deploy" button, allowing users to implement intents one at a time, viewing and testing the resulting configuration before moving on to the next.

---

# Future Vision

Support multiple networking ecosystems through interchangeable platform drivers.

Possible future drivers include:

- Omada
- UniFi
- MikroTik
- pfSense
- OPNsense
- Aruba Instant On

The user experience should remain identical regardless of vendor.

Changing vendors/platforms should require changing only the platform driver—not the user's mental model.

---

# Guiding Principles

1. The canvas is the configuration.
2. Intent before implementation.
3. Vendors are implementation details.
4. Direct manipulation over nested menus.
5. Secure by default.
6. Explain every recommendation.
7. Never require networking expertise.
8. Preview before deployment.
9. The network—not the hardware—is the primary object.