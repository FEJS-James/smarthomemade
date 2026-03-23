---
title: "I Replaced Every Lock in My House With Smart Locks. Here's What Actually Happened."
description: "After swapping all 5 locks for smart locks, I tested Schlage, Yale, and August side by side for 6 months. Here's an honest smart lock comparison with real numbers, what works with Apple, and the best smart lock for 2026."
pubDate: "Mar 20 2026"
tags: ["Smart Locks", "Smart Home", "Security", "Keyless Entry", "Buyer Guide"]
---

Six months ago, I did something my wife called "obsessive" and my locksmith called "job security": I replaced every single lock in my house — front door, back door, garage entry, side gate, and home office — with smart locks. Five doors. Five different locks. One very opinionated verdict.

I didn't do this because I hate keys (though I do). I did it because every smart lock review online reads like a press release. "Great build quality. Easy setup. 4.5 stars." Cool. But does it actually work when your hands are full of groceries at 11 PM in the rain? Does the battery die without warning? Does it phone home to some cloud server every time you unlock your front door?

I tested three of the most popular smart locks in 2026 head-to-head: the **Schlage Encode Plus**, the **Yale Assure Lock 2**, and the **August Wi-Fi Smart Lock (4th Gen)**. I also tried the Aqara U100 and Schlage's new Arrive WiFi Deadbolt. Here's what actually happened — the good, the bad, and the one lock I'd never buy again.

## Why I Went Full Keyless Entry

I've been building out my smart home for years. I run [Home Assistant locally](/blog/smart-home-hub-obsolete-what-to-buy-2026/), I've ditched cloud-dependent cameras for [local NVR setups](/blog/stop-paying-ring-protect-local-cameras/), and I have strong opinions about companies that charge subscriptions for hardware you already own.

Smart locks were the last holdout. I kept a "dumb" deadbolt on the front door because I didn't trust the technology. But after Matter support matured through 2025, and after watching my neighbor fumble with keys while holding a toddler and a pizza for the hundredth time, I decided to go all in.

The rules I set for myself:

1. **No cloud dependency.** If the manufacturer's server goes down, my locks still work.
2. **No subscriptions.** I'm not paying monthly to unlock my own door.
3. **Local control via Home Assistant.** Every lock must integrate without relying on a proprietary bridge.
4. **Physical backup.** Keypad or physical key — I'm not getting locked out of my own house because of a firmware bug.
5. **Works with Apple Home Key.** My wife uses an Apple Watch. If she can't tap-to-unlock, it's a dealbreaker.

## The Contenders: Smart Lock Comparison 2026

### Schlage Encode Plus Smart WiFi Deadbolt — $300

The Schlage Encode Plus has been the smart lock benchmark since its release, and in 2026 it's still the one I recommend to most people. Here's why.

**Build quality is unmatched.** This thing feels like it was designed to survive a battering ram. The ANSI/BHMA Grade 1 certification isn't marketing fluff — it's the highest residential security rating available. Pick it up and you'll feel the difference between this and a $150 lock instantly. The metal construction, the satisfying click of the deadbolt, the tight tolerances — Schlage has been making locks since 1920 and it shows.

**Apple Home Key support works flawlessly.** My wife taps her Apple Watch, the lock opens in under a second. No app, no code, no fumbling. This is the killer feature for any household with Apple devices, and it's the main reason the Encode Plus beats Schlage's newer, cheaper Arrive model (which dropped Apple Home support to cut costs).

**Built-in Wi-Fi means no bridge or hub required.** Pair it directly with your router. It also supports Matter over Wi-Fi as of the late-2025 firmware update, which means it plays nice with Home Assistant, Apple Home, Google Home, and Amazon Alexa simultaneously.

**Battery life: 8 months and counting.** I installed it with a fresh set of 4 AA batteries in September 2025. As of writing (March 2026), I'm at roughly 40% remaining. Schlage claims up to a year, and based on my usage (roughly 10-15 lock/unlock cycles per day on the front door), that tracks.

**The catch:** $300 is steep for a deadbolt. And the keypad, while functional, uses a touchscreen that's occasionally unresponsive in freezing temperatures. At 5°F (-15°C) in January, I had to tap my code twice about 30% of the time. Not a dealbreaker, but worth knowing.

**Verdict: The best smart lock in 2026 for most people.** If you want one lock and don't want to think about it again, [buy the Schlage Encode Plus](https://www.amazon.com/s?k=Schlage+Encode+Plus&tag=smarthomemade-20). It's expensive because it's worth it.

### Yale Assure Lock 2 — $200

The Yale Assure Lock 2 is the smart lock I *wanted* to love more than I do. It's a genuinely good product with one frustrating gap.

**The hardware is excellent.** All-metal construction. Physical button keypad (no touchscreen nonsense — buttons work in every temperature). Quiet motor. The lock/unlock action is noticeably faster and quieter than the first-gen Assure. ANSI Grade 1 certified, same as the Schlage. It comes in multiple finishes and fits standard US deadbolt prep.

**Modular design is clever.** The Yale Assure 2 uses swappable radio modules — you can buy the base lock and add Wi-Fi, Bluetooth, or Matter/Thread connectivity later. This is genuinely smart engineering. I started with the Wi-Fi module and later swapped in the Matter module when I consolidated everything on Thread via Home Assistant. No new lock needed.

**The gap: Apple Home Key requires the Matter module AND an Apple Home hub.** The Schlage Encode Plus does Home Key over its built-in Wi-Fi with zero extra hardware. The Yale requires you to buy the Matter/Thread module ($30 extra) and have a HomePod or Apple TV acting as a Thread border router. It works — and works well — but it's an extra step and extra cost that Schlage doesn't require.

**Battery life: ~6 months.** Slightly shorter than the Schlage in my testing, likely because the motor is faster (more power draw per cycle). Still perfectly acceptable. Uses 4 CR2 batteries, which are slightly more annoying to source than AA.

**Verdict: The best smart lock for Airbnb and rental properties.** The physical keypad makes remote code management dead simple. You can create and delete access codes from the Yale app (or Home Assistant) without being on-site. If you manage a vacation rental, the Yale Assure Lock 2 with the Wi-Fi module is the answer. [Check the Yale Assure 2 on Amazon](https://www.amazon.com/s?k=Yale+Assure+Lock+2&tag=smarthomemade-20).

### August Wi-Fi Smart Lock (4th Gen) — $230

Here's where I get controversial: **I would not buy this lock again.** And I know that's a hot take, because August has legions of fans and gets recommended everywhere. But after six months, I have receipts.

**The good parts first:** August's retrofit design is genuinely clever. You keep your existing deadbolt and key — August replaces only the interior thumb turn with a motorized unit. Installation takes 10 minutes and requires zero modification to your door. If you rent, this is a real advantage. The app is polished. DoorSense (a magnetic sensor that tells you if the door is open or closed, not just locked/unlocked) is a nice feature nobody else offers.

**Now the bad parts.**

**Cloud dependency is baked in.** August's entire architecture routes through their cloud servers. Auto-unlock (the flagship feature that detects your phone approaching and unlocks) requires a constant cloud connection. Remote lock/unlock? Cloud. Activity log? Cloud. Guest access? Cloud. When August's servers had a multi-hour outage in November 2025, my lock's smart features simply stopped working. The physical key still worked, but at that point, why did I spend $230?

**The August app nags you to buy an August Connect bridge** ($50) for remote access, even though the 4th Gen supposedly has Wi-Fi built in. The built-in Wi-Fi is unreliable — my lock disconnected from the network an average of twice per week and required a manual reconnect (pull batteries, reinsert). After four months, I gave up on the Wi-Fi and bought the bridge. Which is a $50 tax on a $230 lock that advertised Wi-Fi as a feature.

**No Matter support. No Home Key. No local API.** In 2026, this is inexcusable. August has been promising Matter support "soon" since 2023. It's not coming. The lock integrates with Home Assistant only through the August cloud integration, which means your automations break when their servers do.

**Battery life: 3-4 months.** Worst of the bunch. The constant Wi-Fi reconnection attempts drain the batteries significantly faster than Schlage or Yale. I went through two sets of CR123A batteries in six months.

**Verdict: Skip it.** The retrofit design is the only thing keeping August relevant, and the Aqara U100 now offers a similar form factor with Matter, Thread, Apple Home Key, and local control. The August is a cloud-first product in a world that's moved on. [If you still want to check it out](https://www.amazon.com/s?k=August+Wi-Fi+Smart+Lock&tag=smarthomemade-20), go in with eyes open.

## The Honorable Mentions

**Aqara Smart Lock U100 ($190)** — Exceptional fingerprint reader, Apple Home Key support, Matter compatible, whisper-quiet motor. The catch: no built-in Wi-Fi, so you need an Apple Home hub or Aqara hub for remote access. If you're already in the Apple ecosystem with a HomePod, this is arguably the best smart lock that works with Apple for the money.

**Schlage Arrive Smart WiFi Deadbolt ($200)** — Schlage's newer, cheaper model. Excellent hardware with great rubber keypad buttons that work in any weather. But it dropped Apple Home Key support, which is a dealbreaker for Apple households. If you don't care about Apple, this is the value pick.

## What I Learned After 6 Months of Keyless Entry

### The stuff nobody tells you:

**Auto-lock is the killer feature, not auto-unlock.** Every review obsesses over geo-fenced auto-unlock. In practice, auto-lock — the lock automatically engaging 30 seconds after the door closes — changed my life more than any other smart home feature I own. I haven't thought about whether I locked the door in six months. That mental load just... disappeared.

**Battery anxiety is real for the first month, then it's not.** All three locks send low-battery warnings weeks before they actually die, and all three have physical key or keypad backup. After the first month, I stopped checking battery levels entirely.

**Guest codes are transformative.** My parents have a code. The dog walker has a code with a schedule (weekdays 11 AM–1 PM only). The cleaner has a code. I can see exactly when each person enters and leaves. No more hiding keys under flower pots. No more getting copies made at Home Depot.

**Smart locks + Home Assistant automations = magic.** When I unlock the front door after sunset, the hallway lights turn on at 40%, the thermostat adjusts from Away to Home mode, and the security cameras switch from Alert to Monitoring. When the last person locks the door and the house is empty, everything reverses. This only works with local control — which is why cloud-dependent locks like August are a non-starter for serious smart home setups. If you haven't set up Home Assistant yet, [here's where to start](/blog/smart-home-hub-obsolete-what-to-buy-2026/).

**Physical security still matters more than smart features.** A $300 smart lock with ANSI Grade 1 certification is meaningfully harder to break into than a $50 deadbolt from the hardware store. But no lock — smart or dumb — will stop a determined intruder who decides to break a window. Smart locks are about convenience and access control, not fortress security. Don't confuse the two. For actual home security that works, [here's what I recommend](/blog/smart-home-security-scam-what-actually-works/).

## The Best Smart Lock in 2026: My Final Ranking

After six months, five doors, and more battery changes than I'd like:

1. **Schlage Encode Plus** — The best overall. Premium build, Apple Home Key, Matter support, no bridge needed, incredible battery life. Worth every penny of the $300 price tag.

2. **Yale Assure Lock 2** — Best for Airbnb/rentals and the best value for non-Apple households. Modular radios, physical keypad, excellent build. The smart lock I'd recommend to anyone on a budget.

3. **Aqara U100** — Best smart lock that works with Apple if you already have a HomePod. Incredible fingerprint reader, quietest mechanism, Matter support. Just needs an Apple Home hub for remote access.

4. **Schlage Arrive** — Best for non-Apple, budget-conscious buyers who want Schlage quality. Great keypad. No Home Key.

5. **August Wi-Fi Smart Lock** — Don't. Cloud-dependent, unreliable Wi-Fi, no Matter, no Home Key, worst battery life. The only advantage is the retrofit design, and Aqara does that better now.

## The Bottom Line

Replacing every lock in my house was the single best smart home upgrade I've made — better than smart lights, better than automated blinds, better than the robot vacuum that terrorizes my cat. The daily quality-of-life improvement is immediate and tangible. No more patting pockets for keys. No more "did I lock the door?" anxiety. No more coordinating key handoffs with guests.

But — and this is the important part — **buy the right lock or don't bother.** A cloud-dependent smart lock that goes dumb when a server hiccups is worse than a regular deadbolt. Demand local control. Demand Matter support. Demand no subscriptions. In 2026, there's no excuse for a smart lock that treats your front door access like a SaaS product.

The [Schlage Encode Plus](https://www.amazon.com/s?k=Schlage+Encode+Plus&tag=smarthomemade-20) is the lock I'd buy five of if I were starting over. The [Yale Assure 2](https://www.amazon.com/s?k=Yale+Assure+Lock+2&tag=smarthomemade-20) is the lock I'd recommend to anyone who asks. And the August is the lock I'm replacing next weekend.

Your keys are obsolete. Make sure their replacement isn't too.

---

*Want to build a smart home that actually works? Start with [the right hub](/blog/smart-home-hub-obsolete-what-to-buy-2026/), ditch [overpriced camera subscriptions](/blog/stop-paying-ring-protect-local-cameras/), and learn [what actually keeps your home secure](/blog/smart-home-security-scam-what-actually-works/).*
