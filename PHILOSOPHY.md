# Philosophy

> [!IMPORTANT]
> This document defines the guiding principles of the NetCanvas project.
>
> Architecture evolves.
> Implementations change.
> Vendors come and go.
>
> These principles should endure.
>
> Whenever multiple technical solutions are possible, contributors should choose the one that best aligns with the philosophy described here.
>
> **Shared philosophy is imperative for shared implementation.**

---

# Our Mission

> **People should design networks—not configure hardware.**

This single sentence is the foundation upon which every NetCanvas design decision should rest.

If a proposed feature requires users to think more like a networking vendor than about their own network, it is probably the wrong feature—or the wrong implementation.

---

# What We Believe

## Networks Are More Important Than Hardware

People build networks.

They do not build collections of switches, routers, access points, and firewalls.

Hardware exists only to implement the network.

NetCanvas should always present the network as the primary object and the hardware as an implementation detail.

---

## Intent Is More Important Than Configuration

Users should describe **what** they want.

NetCanvas should determine **how** each supported platform accomplishes that goal.

Whenever possible, users should think in terms of:

- communication
- relationships
- trust
- services
- topology

—not VLAN IDs, ACL syntax, switch port modes, or vendor-specific terminology.

---

## The Canvas Is the Configuration

The canvas is not documentation.

The canvas is not a planning tool.

The canvas is the desired state of the network.

Moving an object changes the desired state.

Creating a relationship changes the desired state.

Removing a relationship changes the desired state.

Documentation should be generated automatically from the network model—not maintained separately.

---

## Direct Manipulation Is Superior to Nested Configuration

Whenever practical, users should interact directly with the objects they care about.

Prefer:

- drag over browse
- connect over configure
- move over edit
- relationships over property dialogs

The object itself should be the interface.

---

## Complexity Should Be Available—Not Mandatory

Professional networking is inherently complex.

NetCanvas should never pretend otherwise.

Instead, complexity should be progressively disclosed.

Simple tasks should remain simple.

Advanced capabilities should remain available.

Beginners and experts should use the same application—not different applications.

---

## Trust Is More Important Than Automation

Automation is valuable.

Predictability is essential.

Users should always understand what NetCanvas intends to do before anything changes.

Every deployment should be:

- previewable
- understandable
- reviewable
- repeatable

Users should never be surprised by a deployment.

---

## Security Is a Default, Not an Add-On

Secure defaults are better than convenient defaults.

When NetCanvas recommends a safer configuration, it should explain why.

Users should always understand the consequences of overriding a recommendation.

Expert users should retain the ability to make informed decisions.

---

## Help Should Be Available, Not Intrusive

Help should never interrupt the user's workflow.

It should always be immediately available.

Every significant control should answer three questions:

- What is this?
- Why does it matter?
- Should I choose this instead of something else?

Learning should be encouraged.

It should never be forced.

---

## Guidance Is Not Help

Help is initiated by the user.

Guidance is initiated by NetCanvas.

These are fundamentally different systems.

Guidance exists to help users avoid mistakes.

Help exists to help users understand concepts.

Each should be independently configurable.

---

## Vendors Are Implementation Details

NetCanvas should never expose vendor terminology unless the user explicitly requests it.

The canonical network model should remain independent of any specific vendor.

Platform drivers exist to translate intent into implementation.

Changing networking vendors should not require changing the user's mental model.

---

## Documentation Should Never Become Technical Debt

Documentation should be generated from the canonical network model whenever possible.

The network description should always be the authoritative source.

No user should be expected to maintain a diagram separately from the configuration it represents.

---

## Curiosity Should Be Rewarded

NetCanvas should never require networking expertise.

It should always reward curiosity.

Users who wish to understand networking concepts should find explanations everywhere.

Users who do not should never be slowed down.

---

# Decision Framework

Whenever a significant design decision is proposed, contributors should ask:

1. Does this help users express their intent?
2. Does this reduce unnecessary cognitive load?
3. Does this increase trust?
4. Does this keep the network—not the hardware—the primary focus?
5. Would this principle still make sense if every currently supported networking platform disappeared tomorrow?

If the answer to any of these questions is **no**, the proposal should be reconsidered.

---

# What NetCanvas Is Not

NetCanvas is **not**:

- a network diagramming application
- a replacement for existing networking hardware
- another SDN controller
- a vendor-specific management interface
- Infrastructure as Code with a graphical front-end

NetCanvas is a visual, intent-driven network design and configuration platform.

Its purpose is not to hide networking.

Its purpose is to let users think about networking instead of vendor implementation.

---

# Closing Principle

Technology changes.

Networking platforms evolve.

Best practices improve.

The philosophy of NetCanvas should remain constant.

People should design networks.

NetCanvas should determine how those networks are implemented.