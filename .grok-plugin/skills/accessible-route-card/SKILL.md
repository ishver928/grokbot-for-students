---
name: accessible-route-card
description: Format Campus-Pass results as accessible route cards with Maps links. Use whenever a trip plan is ready to show the student.
when-to-use: route card, format the trip, accessibility, wheelchair, step-free
metadata:
  author: Ishanvi Verma
  short-description: Accessible route cards
---

# Accessible route card

Use this exact shape. Keep it readable on a phone.

```markdown
## Route A — cheapest on-time
**Time:** leave [time] · arrive [time] · ~[N] min
**Cost:** [student pass / $X cash] · [why this fare]
**Access:** [step-free / stairs at … / unknown — verify in Maps]

1. Walk [distance] to [stop]
2. [Agency] [route] toward [headsign] · [N] stops to [alight]
3. Transfer at [stop] — wait ~[N] min
4. Walk [distance] to [destination]

**Navigate:** [Google Maps transit link]
**Start Trip:** [one short paragraph from the start-trip skill]
**Emergency:** [one short paragraph from the emergency-help skill]
```

Repeat as **Route B — faster backup** when a second option exists.

## Maps links

Build official direction URLs (encode spaces):

`https://www.google.com/maps/dir/?api=1&origin=ORIGIN&destination=DESTINATION&travelmode=transit`

For a walk-only last mile use `travelmode=walking`. For a bike-share only trip use `travelmode=bicycling`.

If the trip has a transfer, also give a Maps link for the full origin→destination so they can start navigation in one tap.

## Access rules

- Say **step-free** only when Maps or the agency marks the path that way.
- If unknown, write **Unknown — check the wheelchair icon in Google Maps before you leave.**
- Call out long walks, steep hills, gravel paths, and stations known for elevator outages when the source mentions them.
- Keep language concrete: "three stairs at the south entrance," not "may be challenging."
