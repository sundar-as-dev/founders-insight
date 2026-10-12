# Founder's Insight

Notes on business, technology, and building Pagsun — by Sundar Rajan, Founder of Pagsun.

## Format

Each post is a markdown file in this repo with frontmatter:

```md
---
title: Post title
industry: Logistics & Freight   # the client's industry, shown on the post
date: "2026-08-10"
excerpt: A one-sentence summary shown in the listing.
featured: true          # optional; shows it on the home page
ctaTitle: Optional heading for the call-to-action box.
ctaDescription: Optional line under the CTA heading.
disclaimer: Optional note shown at the end of the post. Leave out to show nothing.
challenges:            # optional; shown as a table at the top of the post
  - challenge: What was broken, slow, or risky.
    solution: What we did about it.
impact:                # optional; shown as headline number cards
  - value: 20–30       # the figure, kept short
    label: Bookings handled per day
    before: 5–7        # optional; the figure it replaced
---

Post body in markdown.
```

Posts with `featured: true` appear in the home page's Our Works section,
newest first, up to three. If fewer than three are marked, the newest other
posts fill the gaps, so the section is never empty.

The first `challenges` entry and the first `impact` entry are the primary
ones: the Our Works listing shows them on the case study's cover. Put the
challenge that the headline result answers first. With no `impact`, the cover
shows the first two challenges instead; with neither, the card has no cover.

Posts published here are pulled into [pagsun.com](https://pagsun.com)'s Founder's Insight section.
