Philosophy

[!IMPORTANT]
This document defines the guiding principles of the NetCanvas project.

Unlike implementation details, these principles are intended to remain stable over the lifetime of the project. When multiple technical solutions are possible, contributors should choose the solution that best aligns with the philosophy described here.

Shared philosophy is imperative for shared implementation.

⸻

Why NetCanvas Exists

Professional networking has become increasingly powerful.

It has also become increasingly difficult to understand.

NetCanvas exists because configuring a network should not require users to think like a networking vendor.

Users should think about their network.

NetCanvas should think about the implementation.

⸻

Our Mission

People should design networks—not configure hardware.

Everything in NetCanvas should support this goal.

Whenever implementation details conflict with user intent, user intent takes priority.

⸻

Our Philosophy

Intent Before Implementation

Users should describe what they want.

NetCanvas determines how each supported platform achieves that result.

Vendor terminology belongs inside platform drivers—not in the user’s workflow.

⸻

The Canvas Is the Configuration

The canvas is not documentation.

The canvas is not a planning tool.

The canvas is the desired state of the network.

Documentation should be generated from the network model—not maintained separately.

⸻

Networks, Not Hardware

The network is the primary object.

Routers, switches, access points, firewalls, and controllers exist only to implement the network.

Users should rarely need to think about individual devices unless they intentionally choose to.

⸻

Direct Manipulation

Users should interact directly with the objects they care about.

Whenever possible:

* Drag instead of browse.
* Connect instead of configure.
* Move instead of edit.
* Draw instead of describe.

The object itself should be the interface.

⸻

Progressive Disclosure

Complexity should never be hidden.

It should also never be mandatory.

Simple tasks should remain simple.

Advanced capabilities should always remain available.

Beginners and experts should use the same software—not different software.

⸻

Help Should Empower, Not Interrupt

Help should always be available.

Help should almost never interrupt.

Users should be able to learn at their own pace without slowing experienced users.

Contextual help should answer:

* What is this?
* Why does it matter?
* Should I choose this or something else?

⸻

Guidance Is Different From Help

Help is initiated by the user.

Guidance is initiated by the system.

Guidance exists to prevent accidental mistakes—not to teach networking.

Users should remain in control.

⸻

Security Should Be Understandable

Secure defaults are better than convenient defaults.

Every recommendation should be explainable.

Warnings should explain consequences—not simply prohibit actions.

Expert users should always be able to override recommendations after understanding the implications.

⸻

Trust Is More Important Than Convenience

Users must be able to trust NetCanvas.

Every deployment should be:

* Predictable.
* Explainable.
* Reviewable.
* Reproducible.

The software should never perform surprising actions without making them visible beforehand.

⸻

Vendors Are Implementation Details

NetCanvas should not encourage loyalty to any particular networking ecosystem.

The user’s investment should be in their network design—not in a specific vendor.

Whenever practical, changing hardware should not require changing the user’s mental model.

⸻

Documentation Should Be Automatic

Documentation should not become another task users must remember to perform.

The network model already contains the necessary information.

Documentation should be generated automatically from that model whenever possible.

⸻

Learning Is Optional

NetCanvas should never require networking expertise.

It should always reward curiosity.

Users who wish to understand networking concepts should be able to discover them naturally through contextual explanations.

Learning should be available.

It should never be imposed.

⸻

Making Decisions

When evaluating new features, contributors should ask:

1. Does this help users express their intent more clearly?
2. Does this reduce unnecessary complexity?
3. Does this improve trust?
4. Does this make the network—not the vendor—the primary focus?
5. Would this decision still make sense if every supported networking platform disappeared tomorrow?

If the answer to any of these questions is “no,” the design should be reconsidered.

⸻

Closing Principle

Technology changes.

Networking platforms evolve.

User interfaces come and go.

The philosophy of NetCanvas should remain constant.

People should not have to think like networking vendors.

They should simply design the network they want.

NetCanvas should do the rest.