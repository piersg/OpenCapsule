# OpenCapsule

<img src="opencapsule%20logo%20v.b2.svg" alt="logo" width="250px"/>

(very early) open implementation of most of the Apple Airport Extreme Time Capsule's features

**Status: right now this is just a vaporous planning document**

This is an attempt to recreate most of the (still relevant) features of the Apple Airport Extreme Time Capsule (AETC). Beacuse:
* It does what it does really well. It's small, it's simple, it does a lot
* It's abandonware: the hardware wont last forever; some newer things are refusing to connect to it (e.g. my Ubuntu Framework)

I am envisioning three phases to the development:

## Phase 0 - planning

(which is where we are currently at). Broken down further into:

* Spec it:
  * actually quantify what is good about the AETC, and what we maybe don't need any more (or can't feasibly do in hardware)
  * Then pick some hardware and software (ideally already existing open things that do most of what we want)
* With the hardware and software known, plan the steps in the next 2 sections

## Phase 1 - build it with off the shelf hardware, possibly not that prettily
* do as much software implementation as possible with virtual hardware (which means it's sort-of still planning)
* then do so for real

## Phase 2 - DIY hardware
assuming Phase 1 went well, rustle up some custom hardware that is maybe as compact and elegant as the AETC, within reason. There could be all sorts of things here, but also there's a very real chance we'll give up well before here.


## So what is the AETC and why do I need a modern one?

Maybe a picture sums it up best. Below we have two setups which contain an internet router, ethernet switch, Wifi AP, 3TB NAS (with Time Machine backup capability) and the DC power-supply for the whole setup. On the left is the Apple way of doing that, on the right is everyone else's. My AETC is in my lounge room, behind my TV, it's basically unnoticeable.

As well as being small, the AETC does quite a lot of farily advanced networking (if you want it to) with a very simple interface, there are only about 5 panes to the interface.

But it does have *some* features that maybe we don't need anymore: you can connect a USB printer and it makes it into an airprint one - that sounds really hard to get right and my current printer has wifi. On the hardware side, the integrated power supply, in addition to requring work, would make this unsafe for non-qualified electricians to build.

## So the actual feature list is
* Internet gateway/router with NAT and PPPoE, confirgurable DHCP, port-forwarding (and whatever else is normal)
* Ethernet switch (TBH I only use the ports on the AETC cause they're there and things are close. But it'ś a nice-to-have)
* SMB NAS which can share USB drives of arbitrary size over the network and support Time Machine for macs (and the equivalent for other platforms)
* I'd like it to be cheaper than 

It's not that bif when you look at it!

## Plan - which hardware and software?
The obvious things seem to be a raspberry pi and OpenWrt - they can do the gateway and the NAS out-of-the-box, and I just need to add some ethernet ports to the pi (there are various ways to add them, but for an MVP maybe just buy and gut a small standalone switch and stick it in the box. Our goal here is not world-record performance! This is some games consoles getting updates and some netflix.
