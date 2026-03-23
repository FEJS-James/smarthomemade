---
title: "Matter Was Supposed to Fix Smart Homes. Three Years Later, It's a Beautiful Disaster"
description: "The smart home protocol that promised universal compatibility has delivered fragmentation, confusion, and broken promises. Here's what actually happened to Matter — and what you should do about it."
pubDate: 2026-03-16
---

I remember the keynote. October 2022. The Connectivity Standards Alliance stood on stage and promised us the future: one protocol to rule them all. Apple, Google, Amazon, Samsung — all holding hands, all singing kumbaya, all swearing that Matter would finally make smart home devices Just Work™.

Three years later, I'm staring at a Matter-compatible smart plug that won't pair with my HomePod, a Thread border router that forgot its own network, and a firmware update that bricked my kitchen lights for six hours.

Matter didn't fix the smart home. It added another layer of complexity to an already broken system — and somehow convinced everyone it was progress.

## The Promise Was Intoxicating

Let's be fair about why we all fell for it. The smart home before Matter was genuinely terrible.

Want a Philips Hue bulb to talk to a Ring doorbell? Good luck. You needed Zigbee bridges, cloud accounts, IFTTT recipes, and a prayer to the API gods. Every brand had its own app, its own ecosystem, its own walled garden. Buying a smart home device meant pledging allegiance to a platform.

Matter promised to end all of that. One standard. One setup process. Buy any Matter-certified device, scan a QR code, and it works with any Matter-compatible controller — whether that's Apple Home, Google Home, Samsung SmartThings, or Amazon Alexa.

It sounded perfect. It sounded too good to be true.

Spoiler: it was.

## What Actually Happened

### The Certification Bottleneck

The first crack appeared almost immediately. Getting Matter certification turned out to be expensive, slow, and painful. Small manufacturers — the ones making the interesting, innovative smart home products — couldn't afford the process. The companies that could afford it? They were the same giants who created the fragmentation problem in the first place.

By mid-2024, the list of Matter-certified devices was embarrassingly small. Mostly plugs, lights, and a handful of locks. The "thousands of devices" the Alliance promised? They meant thousands of SKUs from the same dozen companies, many of them just firmware updates slapped onto existing products.

Here we are in 2026, and the situation has improved — slightly. There are now around 1,200 Matter-certified products. Sounds impressive until you realize there are over 50,000 smart home products on the market. Matter covers maybe 2% of what's actually available.

### The "Works With Everything" Lie

This is the one that really stings. Matter was supposed to mean universal compatibility. Device works with Matter? It works with everything.

In practice, it works *differently* with everything.

I tested a Matter-certified smart plug across four ecosystems last month. Here's what happened:

- **Apple Home:** Paired on the third try. Basic on/off and energy monitoring worked. Automations were limited to what Apple Home supports — which, if you've used Apple Home, you know isn't much.
- **Google Home:** Paired on the first try. On/off worked. Energy monitoring? Not exposed. Google's implementation simply doesn't surface certain Matter attributes.
- **Amazon Alexa:** Paired eventually, after a firmware update to both the plug and my Echo hub. On/off worked. Scheduling worked. Energy monitoring was visible but lagged by about 15 minutes.
- **SmartThings:** Refused to pair for 20 minutes. After a factory reset of the plug, it connected. Full feature set available, but the interface was clunky and occasionally showed the device as offline when it wasn't.

One device. Four ecosystems. Four different experiences. Four different feature sets.

This is what "universal compatibility" looks like in practice. The device technically *works* everywhere, but the experience ranges from decent to infuriating depending on which platform you chose. That's not interoperability. That's a shared communication protocol with wildly inconsistent implementation.

### The Multi-Admin Nightmare

Matter's multi-admin feature was supposed to be revolutionary. One device, controlled by multiple ecosystems simultaneously. Your Alexa and your Google Home and your Apple HomePod all controlling the same light — no bridges, no hacks, no compromise.

In reality, multi-admin is the source of more smart home headaches than any single feature I've encountered. Here's why:

When you add a Matter device to multiple controllers, each controller maintains its own state. If you turn off a light via Google Home, Apple Home might still show it as on for several seconds — sometimes minutes. Automations from different controllers can conflict. I've had lights turn on at 11 PM because my Google Home sunset routine and my Apple Home bedtime routine disagreed about what "evening" meant.

The worst part? Debugging multi-admin issues is nearly impossible for a normal person. There's no central dashboard, no unified log, no way to see which controller sent which command. When things go wrong — and they go wrong often — you're reduced to guessing.

My advice? Pick one ecosystem and stick with it. I know that defeats the entire purpose of Matter, but at least your lights will turn on when you ask them to.

### Thread: The Network Layer Nobody Understands

Matter runs on two network types: Wi-Fi and Thread. Wi-Fi you know. Thread is the mesh networking protocol that was supposed to make smart home devices faster, more reliable, and more energy-efficient.

Thread is genuinely good technology. Low-power mesh networking with self-healing capabilities, no single point of failure, and sub-second response times. On paper, it's everything Zigbee and Z-Wave should have been.

The problem isn't Thread itself. It's Thread border routers.

A Thread border router is the device that connects your Thread mesh network to your IP network (and therefore to the internet). Your HomePod Mini is one. Some Nest devices are one. Certain Eero routers are one. And here's where it gets fun: not all Thread border routers play nice with each other.

I have three Thread border routers in my house — a HomePod Mini, a Nest Hub, and a Nanoleaf bulb that apparently doubles as one. Do they form a unified Thread network? Sometimes. When Mercury is in retrograde and I've sacrificed the right number of firmware updates, they cooperate beautifully. Other times, my Thread devices split into separate networks, some devices become unreachable, and I'm back to power-cycling everything like it's 2019.

The Thread Group published a unified specification in late 2025 that was supposed to fix interoperability between border routers from different manufacturers. It helped. It didn't solve the problem. The fundamental issue is that Thread mesh networks are complex, and consumer devices are handling that complexity with varying degrees of competence.

## What Matter Got Right (Because I'm Not Completely Unreasonable)

I've been harsh. Let me acknowledge what's genuinely improved.

**Local control is the default.** This is huge. Before Matter, most smart home devices required cloud connections. Your command went from your phone to a server farm in Virginia and back to the light bulb three feet away. Matter devices communicate locally. The response time improvement alone justifies the protocol's existence.

**Setup has improved.** Scanning a QR code or using NFC to pair a device is genuinely better than the old process of downloading a brand-specific app, creating an account, connecting to a temporary Wi-Fi network, praying, and waiting four minutes for a light bulb to blink twice. Matter's commissioning process isn't perfect, but it's less terrible.

**The big players are committed.** Whatever you think of the implementation, the fact that Apple, Google, Amazon, and Samsung are all investing heavily in the same standard is unprecedented. Previous attempts at smart home unification (Z-Wave Alliance, anyone?) never had this level of industry backing. That commitment means improvement will continue, even if the pace is frustrating.

**Thread is the right foundation.** Once the border router mess gets sorted — and I believe it will — Thread will be the best networking protocol for smart home devices. Period. It's technically superior to Zigbee and Z-Wave in almost every measurable way.

## Why Big Tech Is Quietly Sabotaging Interoperability

Here's the part nobody in the smart home press wants to say out loud: Apple, Google, and Amazon don't actually want perfect interoperability.

Think about it. Apple sells HomePods. Google sells Nest products. Amazon sells Echos. Their business model depends on ecosystem lock-in. If every Matter device works identically across every platform, what's the incentive to buy a HomePod over a Nest Hub? The hardware margins are razor-thin. The real money is in keeping you inside their ecosystem — buying their services, seeing their ads, feeding their data machine.

So what do they do? They implement Matter to the letter of the specification — but not the spirit. They add proprietary features on top. They surface some Matter attributes and hide others. They make pairing *slightly* easier within their own ecosystem. They ensure that a Matter device works best with their controller.

It's not a conspiracy. It's capitalism. And it means that Matter's promise of true interoperability will always be compromised by the companies that control the ecosystems.

This is why I keep coming back to Home Assistant. It's the only major Matter controller that doesn't have a business incentive to limit interoperability. It's open source. It doesn't sell hardware (well, not much). It doesn't need you locked into an ecosystem. It just wants your devices to work.

## What You Should Actually Do in 2026

After three years of testing, hoping, cursing, and factory-resetting, here's my honest advice:

### If You're Starting From Scratch

**Buy Matter-compatible devices, but don't rely on Matter alone.** Choose devices that also support established protocols like Zigbee or Z-Wave as a fallback. The Aqara door sensor, for example, supports both Zigbee and Matter. If Matter fails you — and at some point, it will — you have a backup plan.

**Pick one primary controller and commit.** Multi-admin is a headache. If you're an iPhone household, use Apple Home. Android? Google Home. Want maximum flexibility? Home Assistant. Don't try to use all of them simultaneously unless you enjoy debugging network topologies at midnight.

**Invest in Thread, but keep a Zigbee coordinator.** Thread is the future, but it's not the stable present. A Zigbee coordinator (like the SONOFF Zigbee 3.0 dongle) costs $15 and connects hundreds of proven, reliable devices. Have both.

### If You Already Have a Smart Home

**Don't rip out what works.** If your Zigbee lights have been solid for three years, there is zero reason to replace them with Matter equivalents. I see people in r/smarthome tearing out perfectly functional setups to go all-Matter. This is insane. Your working smart home is not obsolete just because a newer protocol exists.

**Add Matter devices incrementally.** When you need a new device, check if there's a good Matter option. If there is, great — buy it. If the Matter version is more expensive, less feature-rich, or less reliable than the Zigbee/Z-Wave equivalent, buy the established option and don't feel guilty about it.

**Keep Home Assistant in your back pocket.** Even if you primarily use Apple Home or Google Home, having a Home Assistant instance gives you a bridge to everything. It speaks Matter, Zigbee, Z-Wave, Wi-Fi, Bluetooth, and about 2,000 other integrations. It's your insurance policy against any single protocol or ecosystem failing you.

### If You're a Tinkerer

**Run Home Assistant as your primary controller, with Matter as one of many protocols.** This is what I do, and it's the most resilient setup I've found. Home Assistant's Matter integration has improved dramatically since 2024. It's not perfect — some device types still have quirks — but it's the most feature-complete implementation I've tested.

**Build your Thread network deliberately.** Don't just scatter Thread border routers around your house and hope for the best. Place them strategically, use a single brand if possible, and monitor your Thread network topology through Home Assistant's Thread panel. A well-planned Thread network is rock solid. An accidental one is a mess.

## The Uncomfortable Truth

Matter is better than nothing. It's moved the industry forward. Local control as a default is a genuine win. Thread is a genuinely better networking technology. The setup experience, while imperfect, is improved.

But Matter is not the revolution we were promised. It's a compromise — a lowest-common-denominator standard that gives you basic interoperability while each ecosystem silently protects its own interests. The dream of buying any device and having it work perfectly with any controller? We're not there. We might never get there, because the companies that control the controllers don't want us there.

The real winners of the Matter era aren't consumers. They're the same big tech companies that created the fragmentation problem. They get to slap a Matter badge on their products, claim interoperability, and continue building walled gardens — just with a slightly wider gate.

If you want a smart home that truly works for you, that you truly control, the answer in 2026 is the same as it was in 2020: Home Assistant, local protocols, and a healthy skepticism of any corporation that promises to simplify your life.

They're not simplifying your life. They're simplifying their revenue model. And Matter is just the latest tool helping them do it.
