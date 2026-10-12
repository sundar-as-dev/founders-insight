---
title: "The first 30 days after an overnight IT handover: keeping a multi-store hypermarket billing through festival season"
industry: Retail
date: "2025-08-12"
excerpt: How we took over IT for a multi-store hypermarket with no documentation, rebuilt how its tills bill, and got it through a 10x festival rush and a new store opening.
ctaTitle: If your central POS server went down tomorrow, would your tills keep billing?
ctaDescription: Email us and we'll help you find out before it happens.
disclaimer: This engagement covered IT estate audit, incident recovery and managed IT operations only. Penetration testing, security operations (SOC) monitoring and other licensable cybersecurity services are not part of our Managed IT Services. If a client needs them, we point them to a CSA-licensed provider. Risks and gaps are described by type only, and only after they were fixed or accepted, to protect the client.
challenges:
  - challenge: Every POS billed against one central database, so a server or network fault stopped billing at a store.
    solution: An edge server in every store, so each store bills locally and syncs stock and sales with the centre on a schedule.
  - challenge: No documentation of the hardware, network, software, or how billing flowed from warehouse to stores.
    solution: The whole estate mapped layer by layer in one week, then checked against live operations in the second.
  - challenge: No fallback if a store's server or network link failed during trading hours.
    solution: Offline billing on every POS, set up with the ERP vendor, so tills keep working when the systems behind them don't.
  - challenge: Daily backups depended on someone running them by hand after close, and two days were missed before a storage failure.
    solution: The two missing days rebuilt and reconciled, and backups moved to a scheduled job with failure alerts and a runbook with a named owner.
  - challenge: A new store had to open in three months without inheriting the old design.
    solution: Built on fiber end to end with local and offline billing from day one, and run by us for its first three months.
impact:
  - value: 10x
    label: Faster billing across existing stores
  - value: 99.8%
    label: Uptime at the new store, first 3 months
  - value: 30x
    label: Faster billing at the new store, against the old baseline
---

A multi-store hypermarket's IT leadership changed overnight, and the client asked us to step in the same day. There was no handover and no documentation. A festival was a month away, with sales expected at about ten times a normal day, and a new store was due to open in three months. At a single store, a sale goes through roughly every nine seconds. Here is what happened in the first 30 days, and what changed after.

## Day one: no map

Within a day it was clear nothing was written down: not how the stores connected, not how billing flowed from the warehouse to the tills, not how stock synced between locations. We set ourselves two weeks. One to rebuild the map of the estate, layer by layer: hardware, network, software, applications. One to check that map against live operations, because a wrong map is worse than none when the store is full.

## The root cause, by type

Every POS terminal, in every store, on every floor, billed directly against one central database over the private network linking the stores. No store could bill on its own. If the central server slowed down, or a store's network link dropped, billing at that store stopped. Earlier that year, that is how two stores ended up writing bills by hand.

## Billing that keeps going when the network doesn't

We changed the design to three layers:

1. **An edge server in every store.** Each POS bills against its own store's server, and that server syncs stock and sales with the central system on a schedule.
2. **The network stops being a single point of failure.** If a store's link drops, it keeps trading and catches up when the link returns.
3. **Offline billing on every POS.** Working with the ERP vendor's team, we enabled offline mode, so a till can still bill if the store's own server fails.

We built this in under two weeks, which meant finishing the tuning in live production: central-to-store sync, store-to-till sync, and the inter-store links. Billing across the existing stores became about ten times faster.

## The festival, and the failure we hadn't caught

During peak festival trading, the storage on one store's edge server failed. Its disk redundancy had been set up, but not configured correctly, so it didn't carry the load. Billing at that store stopped until we replaced the failed drive and brought the server back, about three hours later.

Then a second problem surfaced. The daily database backup was a manual step after closing, and it had not run for the previous two days. Our data engineers worked with the ERP vendor's team to rebuild and reconcile those two days of sales and stock, until every record matched again.

| When | What happened |
| --- | --- |
| Day 1 | Took over IT leadership with no documentation |
| Days 2–7 | Mapped hardware, network, software and data flows across all stores |
| Days 8–14 | Validated the map against live trading; confirmed the single-database root cause |
| Weeks 3–4 | Edge servers and offline billing live in every store; sync tuned in production |
| Festival peak | Edge storage failure at one store; billing restored in about 3 hours |
| Following days | Two days of missing sales and stock data rebuilt and reconciled |
| Month 3 | New store opened, built on the new design from day one |

## So it can't repeat

Disk redundancy on the edge servers was rebuilt and checked store by store. Backups moved from a manual end-of-day task to a scheduled job that alerts someone when it fails, with a runbook and a named owner. We counted both as our gaps to close: they came from building fast, and they are now part of how we hand over every store.

## The new store, built right from the start

The new hypermarket didn't inherit the old design. We architected, built and ran it for its first three months: edge server and offline billing from day one, and fiber cabling end to end with no copper LAN, so we could see whether the network itself held billing back. It ran at 99.8% uptime over those three months, and bills about 30 times faster than the older stores did before the rebuild.

## What changed

The hypermarket now bills from each store, not from one central database, so a server or network fault stays a local problem instead of a queue at every till. Its IT is documented, its backups alert someone when they fail, and the next store has a design to copy.

*Billing speed measured per bill at the POS, before and after the change. New store uptime measured over its first three months of trading.*
