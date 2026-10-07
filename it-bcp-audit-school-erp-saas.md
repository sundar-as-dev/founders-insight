---
title: An IT estate audit and business continuity plan for a School ERP SaaS provider
category: Managed IT Services
date: "2026-08-10"
excerpt: What we found when we audited the infrastructure behind a School ERP platform, and the BCP plan we built to keep it running.
ctaTitle: Not sure your BCP plan would survive a real outage?
ctaDescription: Email us and we'll walk through an IT estate audit with you.
challenges:
  - challenge: No documented plan for what happens if core infrastructure fails during a school day.
    solution: A business continuity plan built from a full audit of the estate.
  - challenge: Single points of failure across hosting, database, backups, DNS, and integrations that nobody had written down.
    solution: An IT estate audit that mapped every dependency and where it could fail.
  - challenge: A backup process had silently stopped alerting on failure.
    solution: Backup alerting found and fixed during the audit.
  - challenge: 'Domain and DNS renewal lived in one person''s memory.'
    solution: Runbooks with a named owner that someone other than the founder can follow at 11 p.m.
  - challenge: No fallback if the payment provider went down during fee collection week.
    solution: Recovery time targets set for each scenario, with school-hours scenarios like attendance and fee collection prioritised.
---

A School ERP SaaS company came to us with a specific worry: their platform runs attendance, fees, grading, and communication for every school on it, and they had no documented answer for what happens if a core piece of that infrastructure fails during a school day. They asked for two things — an IT estate audit, and a business continuity plan built from what it found.

## Starting with the audit, not the plan

We didn't write the BCP first. A continuity plan built on an incomplete picture of the estate is a plan for the infrastructure you think you have, not the one you actually run. The audit mapped every system the platform depended on — hosting, database, backups, third-party integrations, authentication, DNS — and where each one had a single point of failure that nobody had written down.

## What the audit surfaced

The biggest risks weren't exotic. A backup process that had silently stopped alerting on failure. A DNS and domain renewal step that lived in one person's memory rather than a runbook. An integration with a payment provider that had no documented fallback if the provider had an outage during fee collection week — one of the highest-stakes moments on a school's calendar.

## Building the BCP around real failure modes

The continuity plan was written against the specific failures the audit found, not a generic template. Each scenario got a defined recovery time target, an owner, and a runbook a non-founder could follow at 11 p.m. We prioritized the scenarios that would hit during school hours — attendance and fee collection windows — over ones with more forgiving timing.

## What changed

The company now has a documented, tested answer to "what do we do if X fails," instead of an assumption that someone would figure it out in the moment. The backup alerting gap alone was worth the audit — it's the kind of failure that stays invisible right up until the day it isn't.
