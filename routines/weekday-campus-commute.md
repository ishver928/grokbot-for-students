# Weekday campus commute (optional)

Create this routine only after the student names:

- Campus
- Typical origin (for example a residence hall)
- Typical destination (for example a classroom building)
- Leave-by time
- Time zone
- Confirmation that they want a weekday ping

## Routine text to save

Every weekday at [time] [timezone], plan today's car-free trip from [origin] to [destination] on [campus]. Use live Google Maps transit directions and the university transportation page. Return one route card plus a backup. Include Navigate links, Start Trip, and Emergency. If there is a service alert, a shuttle cancellation, or the usual bus will miss the leave-by time, lead with that. Do not book anything. If live data is unavailable, return `UNVERIFIED_SCHEDULE` instead of yesterday's times.

## Safety

Pause the routine during campus closures and when the student says they are away. Never run Start Trip as if they are already walking unless they ask that day.
