---
title: "6 months at 99.9% uptime: building and managing IT for a 70-person online travel company scaling to 500"
industry: Travel & Hospitality
date: "2026-05-10"
excerpt: How an online travel company went from home Wi-Fi that failed most days to an office network that held 99.9% uptime while headcount grew from 70 to 300.
ctaTitle: Is IT someone's second job at your company?
ctaDescription: Email us and we'll show you what a month of managed IT would look like.
disclaimer: This engagement covered IT infrastructure design and implementation, business continuity planning and six months of managed IT operations only. Penetration testing, security operations (SOC) monitoring and other licensable cybersecurity services are not part of our Managed IT Services. If a client needs them, we point them to a CSA-licensed provider. Risks and gaps are described by type only, and only after they were fixed or accepted, to protect the client.
challenges:
  - challenge: Each floor ran on home broadband and a home Wi-Fi router, so the internet dropped for at least an hour on most days and customer support stopped with it.
    solution: Three SLA-backed leased lines from three providers, on two separate fibre routes plus a wireless link, so no single cable cut takes the office offline.
  - challenge: Overlapping Wi-Fi signals and caps on connected devices slowed everyone down, and the only fix was restarting the router.
    solution: Enterprise wireless across the whole office, handing devices between access points without a reconnect, on redundant managed switches.
  - challenge: Laptops were unmanaged and open to any use, and nobody could see what was using up the bandwidth.
    solution: A primary and standby firewall gateway that balance traffic across all links, fail over automatically and apply web and app access policies by category.
  - challenge: IT problems surfaced only when users complained, and nobody was accountable for fixing them.
    solution: A 24/7 ticketed helpdesk with SLA timings, health monitoring of every network device, and spare laptops for an immediate swap.
  - challenge: Headcount planned to grow from 70 to 500 would outgrow any outside IT partner.
    solution: A documented handover at 300 people, with runbooks and a named owner in a new in-house IT team for every part of the network.
impact:
  - value: "99.9%"
    label: Network uptime over six months
    before: "Under 96%"
  - value: "3"
    label: SLA-backed internet links on separate routes
    before: "0"
  - value: "24/7"
    label: IT helpdesk with SLA timings
    before: None
  - value: "300"
    label: People supported at handover, on a network designed for 500
    before: "70"
---

A 70-person online travel company had no IT team. Its network was a set of home broadband connections and home Wi-Fi routers, and when they failed, the fix was whoever restarted them. Problems surfaced only when the internet dropped and customer calls went unanswered.

## Before we took over

The company worked out of a residential complex: teams on the first and third floors of one block, and another team on the ninth floor of the next. Each floor had its own home broadband line and a home-grade Wi-Fi router that capped how many devices could connect at once. Routers on neighbouring floors overlapped and slowed one another down.

The internet went down for at least an hour on most days, often at peak hours, with everyone online. For a travel company that isn't an inconvenience. A traveller calling about tonight's hotel booking needs an answer now, not when the router comes back.

Laptops were unmanaged too. Anyone could install anything, and if one person's download used up the bandwidth, nobody could see it.

Our assessment was plain: this was a home network, not an organisation's IT infrastructure, and at 100 people it would fail more often, not less.

Then the company raised funding to scale from 70 to 500 people and moved into a commercial office. That gave us a clean start and a clear target: 99.9% network uptime from day one.

## Designing out every single point of failure

We worked layer by layer and asked the same question each time: if this one thing fails, does the office stop?

**Internet.** Three leased lines from three providers, each with an SLA and an escalation matrix. Two providers alone aren't enough if both cables run down the same road, because one excavation can cut both. So the two fibre lines reach the building by different routes, and the third connection is a wireless link that doesn't depend on a cable at all.

**Gateways.** Behind the lines sit two firewall gateways with the same configuration. They balance traffic across all three links and, if one drops, send everything through the ones still up, without anyone touching anything. The primary is a high-end unit; the standby is smaller but carries the office if the primary fails. They also apply the company's web and app access policy by category and keep access logs under that policy.

**Inside the office.** We put two designs in front of the client: wired desks separated into VLANs, or a fully wireless office. With headcount rising fast and unpredictably, people moving across the floor all day, and a budget to respect, they chose wireless. That meant only four managed switches, redundant units included, and enterprise access points that pass a laptop or phone from one to the next as people walk, without dropping the connection.

**Devices.** Laptops, CCTV and biometric attendance are managed centrally, with access granted by role. A pool of spare laptops means a failed machine is swapped, not waited on.

**Power.** Backup power stayed with the facilities team. We wrote that boundary into the plan so neither side assumed the other had it covered.

## What we ran every month

For six months after go-live, we ran the infrastructure ourselves:

- A 24/7 IT helpdesk with a ticketing system and SLA timings for every request
- Health monitoring of links, gateways, switches and access points, so most issues were fixed before a user reported them
- Immediate laptop replacement from the spare pool when a machine failed
- A monthly review of uptime, tickets and capacity against the hiring plan

## Six-month service scorecard

| Area | What we committed to | What we delivered |
| --- | --- | --- |
| Network uptime | 99.9% | 99.9% across six months, with several months at 100% |
| Internet links | No single cable cut takes the office offline | 3 lines, 3 providers, 2 fibre routes plus 1 wireless |
| Gateway failure | Traffic keeps flowing without manual work | Primary and standby gateways, same configuration |
| Wi-Fi | Move across the office without reconnecting | Enterprise access points on 4 managed switches, redundancy included |
| Laptop failure | Back to work immediately | Swap from the spare pool |
| IT support | Around the clock, with response times | Ticketed helpdesk, 24/7, with SLA timings |

*Measured over six months of managed operation, from go-live to handover.*

## Handing over at 300 people

By month six the company was nearing 300 people and still hiring. At that size, IT needs people on site who report to the company's own leadership. We recommended an in-house IT team with its own lead, documented the network, configurations and runbooks, and handed each part to a named owner who could run it without us.

## What changed

The company went from a network that failed most days to one that held 99.9% uptime while headcount more than quadrupled. Its support team spent those six months looking after travellers instead of restarting routers, and IT showed up only in a monthly report.
