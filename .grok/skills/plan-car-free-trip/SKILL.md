---
name: plan-car-free-trip
description: Plan a realistic car-free trip for a college student. Use when they name two places, a campus, a time, or ask how to get somewhere without a car.
when-to-use: trip, route, how do I get to, bus, shuttle, transit, no car, campus to downtown
argument-hint: "[campus] from [origin] to [destination] at [time]"
metadata:
  author: Ishanvi Verma
  short-description: Car-free trip plan
---

# Plan a car-free trip

## When to use

The student wants to go somewhere and should not need a car.

## Required inputs

- Campus or city
- Origin (building, address, or "I'm on campus")
- Destination
- When they need to arrive or leave
- Access needs (wheelchair, no stairs, limited walking, traveling at night)
- Whether they have a student transit pass / campus ID

If campus, origin, or destination is missing, stop with `NEED_CAMPUS` or `NEED_PLACES`. Do not guess a school.

## Sequence

1. Identify the campus transportation page and the regional transit agency. Open them in the browser when available.
2. Check student fare programs with the `university-transit-benefits` skill before quoting cash fares.
3. Get live or same-day directions in Google Maps with **transit** (and walking/biking if that is shorter and safe).
4. Build two options when they exist: **cheapest that still arrives on time**, then **faster backup**.
5. Format both with the `accessible-route-card` skill.
6. Attach Start Trip and Emergency using those skills. For evening or isolated stops, Emergency is mandatory, not optional.
7. If the last vehicle of the night is before they can leave, say so. Offer safe-ride, a morning option, or (only then) that a car/rideshare may be safer.

## Validation

- Every vehicle leg has an agency, route number or name, and direction if Maps or the agency site showed one.
- Walking legs have an approximate distance or time.
- If you could not open live data, mark the card `UNVERIFIED_SCHEDULE`.
- Never add a fictional shuttle "that campuses usually have."

## Return

A route card pack in the current conversation. No booking. No "I reserved this for you."
