---
name: start-trip
description: Give a 10-minute leave-now checklist and open navigation. Use when the student says they are ready to go, Start Trip, or "I'm leaving now."
when-to-use: start trip, leaving now, navigate, walk me there, I'm heading out
metadata:
  author: Ishanvi Verma
  short-description: Start Trip checklist
---

# Start Trip

## Goal

Get them moving with current info, not a plan from an hour ago.

## Sequence

1. Re-open Google Maps transit directions for origin → destination **now**. If the vehicle they were going to take has already left, rebuild the card. Do not send them to a departed bus.
2. Tell them the leave-by time, the first stop name, and which side of the street / campus entrance.
3. Remind them: student ID / pass, charged phone, headphones out while crossing, and a backup vehicle if they miss this one.
4. Hand them the Navigate link. One tap.
5. If it is dark, isolated, or the wait is more than ~15 minutes, add the Emergency block and mention campus safe-ride if the school runs one tonight.

## Copy shape

**Start Trip:** Leave by [time]. Walk to [stop]. Take [route] toward [headsign] at [time]. If it does not arrive by [time + 8 min], open Maps and take [backup]. Keep your campus ID out for the farebox.

## Do not

- Do not start a trip if they reported danger — switch to `emergency-help`.
- Do not keep them on a missed connection. Recalculate.
