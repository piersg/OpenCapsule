# OpenCapsule

<img src="opencapsule%20logo%20v.b2.svg" alt="OC Logo" width="250px"/>

(very early) open implementation of most of the Apple Airport Extreme Time Capsule's features

**Status: Still mostly just an idea**

This is an attempt to recreate most of the (still relevant) features of the Apple Airport Extreme Time Capsule (AETC). Beacuse:
* It does what it does really well. It's small, it's simple, it does a lot.
* It's abandonware: the hardware wont last forever; some newer things are refusing to connect to it (e.g. my Ubuntu Framework).

Still in its very days, my current thinking is this will be a project in 2 parts:
1. A OpenWRT package to implement the cut-down (yet powerful!) interface features (not an exact copy, of course). This should run on any hardware that OpenWRT supports but actually confirming/testing that is not a goal of the project.
2. A relatively narrowly defined hardware platform (probably a Raspberry Pi and some peripherals) which is the "standard" platform and the one we build and test on.

## Exact current status
Phase 1a - software MVC (see [plan](PlanRationale.md) for more). I have OpenWRT running in a virtualised Pi and I'm about to start learning how to make a plugin for it. Deciding if one could simply skin Luci or make a plugin for it, or if a whole separate UI is better. It could be a while.

Hardware is expected to be a Raspberry Pi (not sure which model will be good enough) plus some extra ethernet ports but the challenges of fitting all that into a compact enclosure *might* mean we skip straight to custom hardware. If we get that far.

There is some further reading here while you wait (but I wouldn't call that finished either), start with the [original readme/rationale](PlanRationale.md) docuemt