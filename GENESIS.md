# Genesis

> *Every project has an origin story.*
>
> This document captures how NetCanvas evolved from a simple idea into a new way of thinking about network configuration.

---

# The Beginning

NetCanvas did not begin as NetCanvas.

It began as **NCMM (Network Configurator for Mere Mortals)**.

The original objective was modest:

> Make TP-Link Omada easier to configure.

The initial concept centered around simplifying Omada's existing configuration workflow. Rather than forcing users to navigate the Omada Controller's numerous menus and dialogs, NCMM would present a simpler interface and somehow translate the user's intentions into Omada configuration.

At first, several possible implementation strategies were considered:

- Manipulating Omada backup files
- Modifying the controller database directly
- Reverse engineering Omada's internal APIs

Those ideas solved **how** to change Omada.

They did not solve **why configuring networks is difficult in the first place.**

That realization changed everything.

---

# The First Turning Point

The project stopped asking:

> "How do we configure Omada?"

and started asking:

> "Why does the user have to think about Omada at all?"

Omada was never the problem.

UniFi would present many of the same challenges.

So would MikroTik.

So would pfSense.

Every networking platform exposes its own terminology, its own menus, and its own implementation details.

Users are forced to think like the vendor.

NetCanvas should allow them to think about **their network instead.**

---

# The Canonical Model

Once the project shifted from vendor-specific thinking to network-centric thinking, another realization followed.

Every networking platform has different terminology.

But they all implement fundamentally similar concepts.

For example:

- Networks
- VLANs
- Devices
- Services
- Communication Policies
- VPNs
- DHCP
- DNS

Those became the foundation of the canonical model.

Vendor-specific concepts belong only inside platform drivers.

The user should never need to understand how Omada, UniFi, or any other platform chooses to implement those concepts.

---

# Terraform Was an Inspiration, Not a Goal

During early architectural discussions, Infrastructure as Code tools such as Terraform became an important reference.

Terraform demonstrated an architectural pattern:

Desired State

↓

Diff Engine

↓

Provider

↓

Platform

NetCanvas adopts the same philosophy while pursuing a completely different user experience.

Terraform assumes the user writes code.

NetCanvas assumes the user draws.

---

# The Biggest Realization

At one point the project was described as:

> "A network CAD program."

That simple phrase changed everything.

Traditional network diagrams document an existing network.

NetCanvas does something fundamentally different.

The canvas is **not documentation.**

The canvas **is the configuration.**

Moving an object changes the desired state.

Deleting a relationship changes the desired state.

Drawing a new connection changes the desired state.

Documentation becomes an automatic by-product of configuration rather than a separate artifact that inevitably becomes outdated.

This became the defining philosophy of the project.

---

# A Shift in Perspective

Most network management software is device-centric.

Users configure:

- Routers
- Switches
- Access Points
- Firewalls

NetCanvas is network-centric.

Users manipulate:

- Devices
- Networks
- Relationships
- Communication

The hardware becomes an implementation detail.

---

# Direct Manipulation

The user should interact directly with the objects they care about.

Examples:

- Drag a device into a VLAN.
- Draw a connection between two objects.
- Group multiple devices together.
- Remove a relationship.

The user should rarely need to search through nested menus.

The object itself should be the interface.

---

# Progressive Disclosure

Professional networking contains enormous complexity.

NetCanvas should not hide that complexity.

It should reveal it only when necessary.

Every object should expose three levels of interaction.

## Quick Actions

Common operations.

Rename.

Duplicate.

Delete.

Enable.

Disable.

---

## Properties

The normal editing experience.

Most users should rarely need anything else.

---

## Advanced

Vendor-specific options.

Platform-specific capabilities.

Expert tuning.

The complexity remains available without overwhelming users who don't need it.

---

# Help Is Always Available

One of the earliest design goals was to make networking approachable.

Initially, this suggested a highly guided experience.

Further discussion led to a better philosophy.

Help should never interrupt.

Help should always be available.

Every dialog, control, option, and field should provide contextual help through a simple help icon.

Good help answers three questions.

- What is this?
- Why does it matter?
- Should I choose this or something else?

Users remain in control of when they learn.

---

# Guidance Is Different From Help

Another important realization was that help and guidance are separate concepts.

Help is initiated by the user.

Guidance is initiated by the system.

Examples of guidance include:

"This configuration would expose your management network."

"Most camera VLANs should not have unrestricted Internet access."

Guardrails exist to prevent accidental mistakes.

They are not tutorials.

---

# Experience Profiles

No single user experience fits everyone.

NetCanvas should support configurable experience profiles.

## Guided

Maximum assistance.

Wizard-based workflows.

Intent-driven dialogs.

AI assistant enabled.

Verbose explanations.

---

## Standard

The recommended default.

Contextual help everywhere.

Security guardrails enabled.

Minimal interruptions.

---

## Expert

Fast workflow.

No wizard prompts.

Minimal confirmations.

Advanced options always visible.

---

Profiles are merely starting points.

Every user should be able to customize every behavior.

---

# Deployment Philosophy

Configuration changes should never be hidden.

Before deployment, NetCanvas produces a deployment plan.

For example:

- Create VLAN 22
- Create DHCP Scope
- Move Tahiti into VLAN 22
- Create IP Group
- Update ACL

Users should understand exactly what will happen before anything changes.

An optional step-by-step deployment mode should allow each planned change to be applied individually, giving users the opportunity to validate the network after every step.

This makes experimentation safer and troubleshooting dramatically easier.

---

# The UI Is the Product

One of the most important architectural decisions was recognizing that NetCanvas is **not** an automation engine with a graphical interface.

The graphical interface *is* the product.

Everything beneath it exists for one purpose:

To make the canvas trustworthy.

The deployment engine.

The canonical model.

The diff engine.

Platform drivers.

These are all implementation details supporting the experience presented by the canvas.

---

# Looking Forward

Although NetCanvas began with TP-Link Omada in mind, the architecture intentionally avoids vendor lock-in.

Future platform drivers may include:

- TP-Link Omada
- Ubiquiti UniFi
- MikroTik
- pfSense
- OPNsense
- Aruba Instant On
- Additional platforms as the project evolves

Adding support for a new platform should require writing a new driver—not redesigning the application.

The user's mental model should remain unchanged regardless of the hardware beneath it.

---

# Guiding Principles

1. The canvas is the configuration.
2. Intent before implementation.
3. Vendors are implementation details.
4. Direct manipulation over nested menus.
5. Progressive disclosure over unnecessary complexity.
6. Help should always be available but never intrusive.
7. Guidance should protect users without taking control away from them.
8. Secure defaults are better than convenient defaults.
9. Preview before deployment.
10. The network—not the hardware—is the primary object.
11. Documentation should be generated automatically from the network model.
12. Users should never be required to think like the vendor.

---

# Closing Thoughts

NetCanvas is an attempt to change the way people think about configuring networks.

Instead of asking users to learn the language of every networking vendor, NetCanvas allows them to express their intent visually.

The software assumes responsibility for translating that intent into platform-specific configuration.

The ultimate measure of success will not be how many platforms NetCanvas supports.

It will be whether users stop thinking about configuring routers, switches, and access points...

...and simply start drawing the network they want.