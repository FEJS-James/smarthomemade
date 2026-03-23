---
title: "Smart Home Security Is a $10 Billion Scam — Here's What Actually Stops Burglars"
description: "The smart home security industry sells fear and subscriptions. After researching real burglary data, testing DIY systems, and talking to actual cops, here's what really protects your home — and what's just expensive theater."
pubDate: "Mar 21 2026"
tags: ["Smart Home", "Security", "Home Security", "DIY Security", "Privacy"]
---

Let me tell you about the most expensive lesson I almost learned.

Last year, I nearly dropped €2,400 on a professionally installed smart home security system. Monthly monitoring at €30. A three-year contract. A salesman who showed up uninvited after I moved into my new house — because someone at the municipality's registration office apparently sells address lists to security companies. Lovely.

He had a slick iPad presentation. Motion sensors. Glass break detectors. 24/7 professional monitoring. A panic button. And the centerpiece: if someone breaks in, the monitoring center calls the police for you.

Sounds reasonable, right? Except I did something radical. I asked questions. And the whole thing fell apart.

## The Dirty Secret: Professional Monitoring Is Mostly Theater

Here's what the security industry doesn't want you to think about too hard: **the average police response time to a residential burglar alarm is 7 to 15 minutes.** In many cities, it's longer. In Berlin, where I live, the average response to a non-emergency alarm call is north of 20 minutes.

Now here's the kicker: **the average residential burglary takes 8 to 12 minutes**, according to FBI UCR data and Eurostat crime surveys. Most burglars are in and out in under 10 minutes. They're not cracking safes like in the movies. They're grabbing laptops, jewelry, cash, and small electronics — and they're gone before anyone with a badge shows up.

So what exactly is professional monitoring buying you? A phone call. Someone at a call center in who-knows-where sees an alert, tries to call you, waits for you to not answer, then calls the police. By the time a patrol car rolls up, the burglar is three neighborhoods away.

But wait — it gets worse.

**False alarm rates for residential security systems run between 94% and 98%** depending on whose data you trust. The International Association of Chiefs of Police puts it at 94-99%. This means police departments have learned to deprioritize alarm calls. Many US cities now fine homeowners for repeated false alarms — $50 for the first, up to $500 for repeat offenders. Some departments have stopped responding to unverified alarms entirely.

You're paying €30/month for the privilege of being deprioritized by emergency services.

## What Burglars Actually Do (It's Not What ADT Wants You to Think)

I spent way too long reading criminology research for this article. Here's what the data actually says about how burglaries happen:

**1. Most burglaries are crimes of opportunity, not planned heists.**

A University of North Carolina at Charlotte study surveyed 422 convicted burglars. The findings demolish most security industry marketing:

- 83% said they checked for an alarm system before breaking in
- But only 60% said alarms would deter them from a specific target
- **They simply moved to the next house without one**
- The top deterrent wasn't alarms — it was **signs of occupancy** (lights on, car in driveway, TV sounds)

**2. Entry points are boringly predictable.**

- 34% enter through the front door (often unlocked)
- 23% through a first-floor window
- 22% through the back door
- The rest through garages, basements, or second-floor windows

A third of burglaries happen through an **unlocked door.** No amount of smart sensors helps if you leave the front door open.

**3. Burglars avoid confrontation above everything.**

Burglaries overwhelmingly happen during the day, between 10 AM and 3 PM, when people are at work. Burglars don't want to encounter anyone. The moment they think someone's home, they leave.

This is the critical insight that the entire smart home security industry either ignores or buries: **the appearance of presence is more effective than any sensor, camera, or monitoring service.**

## The Smart Home Security Stack That Actually Works

After going down this rabbit hole, I scrapped the professional security plan entirely. Instead, I built a DIY security setup that costs a fraction of what ADT or Verisure charges — with zero monthly fees, zero cloud dependency, and based on what actually deters break-ins according to, you know, science.

Here's my stack:

### Layer 1: Physical Deterrence (Total Cost: ~€250)

This is the unglamorous stuff that security companies never mention because there's no recurring revenue in it.

**Reinforced door frames and strike plates — €60**

Most front doors are kicked in, not picked or hacked. A standard strike plate is held by two screws barely an inch long, driven into soft pine door frames. A solid kick breaks them instantly.

I replaced every exterior strike plate with a 3mm steel reinforcement plate secured by 75mm screws that reach the structural studs behind the frame. This single upgrade — which took 20 minutes per door — makes a forced entry dramatically louder, harder, and slower. A burglar expecting one kick now needs sustained effort, making noise, attracting attention.

This is boring. It doesn't have an app. You can't check it from your phone. **It's also more effective than any smart sensor ever made.**

**Security film on ground-floor windows — €120**

Window security film doesn't make glass unbreakable, but it holds shattered glass together, turning a quick smash-and-reach into a prolonged, noisy wrestling match with a stubborn window. Most burglars will try once, see it's not giving way, and bail.

**Exterior motion-activated lights — €70**

Four solar-powered motion lights covering all entry points. Burglars hate light. It's that simple. A 2015 study from the College of Policing in the UK found that improved street lighting reduced crime by 21% in treated areas.

Total for physical deterrence: about €250, one-time cost, no subscriptions, no batteries to maintain (solar lights), no apps to update, no cloud servers to go down.

### Layer 2: Smart Detection (Total Cost: ~€450)

Now we get into the smart home territory — but notice it's Layer 2, not Layer 1. The fancy tech supplements physical security. It doesn't replace it.

**Local-recording security cameras (Reolink RLC-810A × 3) — €270**

I covered this in detail in my article on [cameras that don't need subscriptions](/blog/stop-paying-ring-protect-local-cameras/), but the short version: three Reolink PoE cameras cover the front, back, and side of the house. They record to a local NAS. No cloud. No subscription. No footage getting handed to police without my consent (looking at you, [Ring](/blog/ring-doorbell-snitching-privacy-2026/)).

The cameras serve dual purposes: they record evidence if something does happen, and — more importantly — the visible presence of cameras is itself a deterrent. The UNC Charlotte study found that visible cameras were among the top five deterrents cited by convicted burglars.

**Zigbee door/window sensors (Aqara × 8) — €80**

Eight contact sensors on every exterior door and accessible window. These connect to my [Home Assistant setup](/blog/smart-home-hub-obsolete-what-to-buy-2026/) via a Zigbee coordinator. When any sensor triggers while I'm away, I get an instant notification on my phone — no monitoring center middleman, no 60-second verification delay.

**Zigbee motion sensors (Aqara FP2 × 2) — €100**

Two mmWave presence sensors covering the main entry hallways. These detect human presence even if someone is standing still — unlike PIR sensors that only detect movement. They're also smart enough to differentiate between my cat and a person, which eliminates the false alarm problem that plagues traditional systems.

### Layer 3: Smart Response (Total Cost: €0 — Just Automations)

This is where Home Assistant earns its reputation as the [best smart home hub](/blog/smart-home-hub-obsolete-what-to-buy-2026/). I've built automations that respond to security events — and they're more effective than a monitoring center because they're instant.

**Automation 1: "The house is alive"**

When the alarm triggers (any door/window sensor while in "away" mode), the following happens simultaneously:

- All interior lights flash on and off twice, then stay on
- The living room TV turns on to a news channel at high volume
- The smart speaker announces "SECURITY ALERT — RECORDING IN PROGRESS" in a loud, authoritative voice
- All exterior lights go to maximum brightness

This creates the single most effective burglary deterrent: **the appearance that someone is home and aware.** The flashing lights are visible from outside. The TV audio is audible through walls. The announcement makes it clear they've been detected.

Most burglars at this point are already running.

**Automation 2: "The evidence collector"**

Simultaneously:

- All cameras switch to maximum resolution continuous recording
- A 30-second video clip from each camera is captured and sent to my phone via Telegram
- A snapshot is sent to my email (redundant backup)
- My phone gets a critical alert with camera feeds

I receive actionable information — actual video of what's happening — within 5 seconds. Not a phone call from a monitoring center asking for my verbal password while I panic.

**Automation 3: "The neighbor alert"**

If I don't dismiss the alert within 60 seconds, Home Assistant sends a pre-written message to two trusted neighbors asking them to check on the house. Real humans, physically nearby, who can actually see what's going on.

**Automation 4: "Vacation mode"**

When we're traveling, a randomized presence simulation runs automatically:

- Lights turn on/off in realistic patterns throughout the evening
- The TV turns on during typical viewing hours
- Blinds open and close on a schedule offset by ±15 minutes each day
- The front porch light follows a sunset-triggered schedule

This isn't a lamp on a timer from 1995. It's a dynamic simulation that changes daily, includes realistic room-to-room movement patterns, and is indistinguishable from actual occupancy to a casual observer.

## The Real Cost Comparison

Let's do the math that security companies hope you never do.

### Professional Monitored System (ADT/Verisure Equivalent)

| Item | Cost |
|------|------|
| Equipment + installation | €500–€1,500 |
| Monthly monitoring (36-month contract) | €30/month = €1,080 |
| First three years total | **€1,580–€2,580** |
| Years 4–10 (ongoing monitoring) | **€2,520** |
| **10-year total** | **€4,100–€5,100** |

Plus you get: cloud dependency, privacy concerns, false alarm fines, deprioritized police response, and equipment you probably don't own (some contracts require returning it).

### My DIY Setup

| Item | Cost |
|------|------|
| Physical deterrence (strike plates, film, lights) | €250 |
| Cameras (Reolink × 3) | €270 |
| Door/window sensors (Aqara × 8) | €80 |
| Motion sensors (Aqara FP2 × 2) | €100 |
| Home Assistant Green (if you don't have one) | €100 |
| **Total** | **€800** |
| Monthly cost | **€0** |
| **10-year total** | **€800** (+ maybe €100 for replacement sensors) |

For less than the installation cost of a professional system, I have a setup that:

- Responds faster (instant vs. 60+ seconds)
- Has fewer false alarms (mmWave > PIR)
- Gives me actual video, not a phone call
- Works without internet (Zigbee is local)
- Doesn't share data with anyone
- Has no contract, no cancellation fees, no monthly drain

## "But What About the Professional Response?"

This is the last refuge of the security industry sales pitch. "Sure, you can DIY the cameras and sensors. But who's going to call the police?"

My phone is. Immediately. With video evidence.

When I call the police with "I have a live camera feed showing someone breaking into my house right now, I can see them, here's what they look like," that gets a very different response than when a monitoring center calls with "We have an unverified alarm activation at this address, the homeowner didn't answer the phone."

In 2026, your phone is the monitoring center. Push notifications are instantaneous. Video is streamable from anywhere. If you need to escalate, you do it yourself, with evidence, and you get taken seriously.

## The Brands That Are Worst at This

I'm going to name names because someone should.

**ADT** charges up to $60/month in the US for "premium" monitoring that includes... the same delayed phone-call-then-police-call routine. They've been fined multiple times for deceptive practices, including a 2024 FTC settlement for misleading customers about their monitoring capabilities. Their technicians have been caught [accessing customer cameras without authorization](https://www.ftc.gov/news-events/news/press-releases/2024/03/adt-agrees-pay-25-million-settle-ftc-charges). Inexcusable.

**Ring** (Amazon) has turned doorbell cameras into a neighborhood surveillance network that [shares footage with police](/blog/ring-doorbell-snitching-privacy-2026/) — often without warrants. They've built a business model on fear, with their Neighbors app serving as a 24/7 crime anxiety amplifier that makes people think their street is a war zone so they'll buy more cameras.

**Verisure** (Securitas Direct) in Europe operates on the same model: expensive installation, mandatory multi-year contracts, monthly fees that add up to thousands, and equipment you don't own. Their cancellation process is deliberately hostile.

All three companies share a common business model: **sell fear, then sell the subscription cure.**

## What I'd Tell My Neighbor

If my neighbor asked me "should I get a security system?", here's exactly what I'd say:

1. **Lock your doors.** Seriously. A third of burglaries are through unlocked doors. A smart lock with auto-lock ([like the ones I tested](/blog/smart-lock-replacement-what-actually-happened/)) solves this permanently.

2. **Reinforce your frames and add window film.** €180, one afternoon, massive impact.

3. **Put up visible cameras.** Even dummy cameras deter opportunistic burglars — but real ones with [local recording](/blog/stop-paying-ring-protect-local-cameras/) are better because you actually get evidence.

4. **Make your house look occupied when you're away.** Smart lights and a [Home Assistant setup](/blog/smart-home-hub-obsolete-what-to-buy-2026/) can automate this convincingly.

5. **Know your neighbors.** The single most effective security measure in existence is a community that watches out for each other. No app required.

6. **Don't sign a monitoring contract.** You're paying for a slower, less capable version of what your phone already does for free.

## The Bottom Line

The smart home security industry is built on a simple psychological exploit: fear of break-ins makes people irrational buyers. When you're scared, a €30/month "monitoring fee" feels like a small price for peace of mind.

But peace of mind shouldn't cost €360 a year for a service that objectively underperforms what you can build yourself for a one-time €800 investment. The data is clear. Physical deterrence and the appearance of occupancy stop burglaries. Smart detection and instant personal alerts handle the rest. Professional monitoring is an expensive middleman adding latency to a process that needs to be instant.

Your home doesn't need a security company. It needs reinforced doors, visible cameras, smart automations, and you — with a phone full of instant alerts and live video.

The security industry won't tell you this, because a one-time €800 customer is worth a lot less than a €360/year subscriber locked into a three-year contract.

Now you know. Act accordingly.

---

*Building your own security setup? Start with [cameras that don't charge monthly](/blog/stop-paying-ring-protect-local-cameras/) and a [Home Assistant hub](/blog/smart-home-hub-obsolete-what-to-buy-2026/) that keeps everything local. Your wallet — and your privacy — will thank you.*
