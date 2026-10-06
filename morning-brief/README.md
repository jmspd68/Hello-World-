# Morning brief agent

A Claude Code routine that renders a calm, one-page morning brief every weekday.

## Schedule

- **When:** weekdays at 6:47 AM, America/New_York (`CRON_TZ=America/New_York 47 6 * * 1-5`)
- **How:** each run starts a fresh cloud session and uses the `anthropic-skills:morning` skill
- **Notifications:** push notification when a run finishes
- **Routine ID:** `trig_01FPFV4sWLKrEocnLGT4J6zf` (manage it at claude.ai/code → Routines)

## What the brief contains

1. **Visual anchor:** the day's calendar drawn as terrain (heavy, normal, or open), with three time "acts"
2. **Needs attention:** email threads waiting on you, things that close today, and prep for tomorrow
3. **Resolved:** things that recently closed, so you can skip them

## Sources

| Role     | Connector                                  |
|----------|--------------------------------------------|
| Calendar | Google Calendar (primary + Family)         |
| Email    | Gmail                                      |
| Chat     | none yet; connect Slack to add mentions/DMs |

> **Note:** the routine must have the Gmail and Google Calendar connectors
> attached, otherwise scheduled runs can't read your data. Add them from the
> routine's settings at claude.ai/code → Routines → *Morning brief*.

## Prompt

See [`prompt.md`](./prompt.md).
