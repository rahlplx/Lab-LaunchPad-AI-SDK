---
name: growth-check
description: Ask the founder's current user count and recommend stage-appropriate next actions (0-100, 100-1000, 1000-10000+ users), instead of treating every project the same regardless of scale. Use periodically post-launch, or whenever the founder asks what to focus on next.
---

# Growth Check

The right thing to focus on at 10 users is not the right thing to focus
on at 5,000. This skill exists so a founder isn't given generic advice
disconnected from where they actually are.

## What to do

1. **Ask the current user count directly** — a rough number is fine,
   this doesn't need to be precise. Don't infer it from unrelated
   conversation; ask.

2. **Place it in one stage and recommend accordingly:**
   - **0-100 users:** Talk to users directly, by name if possible. Focus
     entirely on `/process-feedback` and fixing what's actually blocking
     the people you have, not on scale-readiness work.
   - **100-1,000 users:** Start looking for repeatable acquisition (which
     channel from `/plan-launch` is actually working, not just which was
     tried), and start caring about `/check-costs` more seriously as
     usage-based bills start to add up.
   - **1,000-10,000+ users:** Focus shifts toward reliability and
     `/setup-monitoring` mattering more than new features — at this
     scale, an outage or a bad regression affects real numbers of real
     people, not a handful of early adopters who'll forgive a rough edge.

3. **Name what NOT to worry about yet**, explicitly, for their stage —
   e.g. a founder at 40 users doesn't need a formal on-call rotation; a
   founder at 8,000 shouldn't still be manually reading every single
   piece of feedback line by line without `/process-feedback`'s
   prioritization.

4. **Don't recommend scale-readiness work preemptively.** Building for
   10,000 users while at 50 is a common, expensive founder mistake this
   skill exists partly to prevent.

## Anti-patterns to avoid

- Giving the same generic "growth advice" regardless of stated user
  count.
- Recommending infrastructure/reliability investment far ahead of actual
  scale.
- Treating this as a one-time check — the right answer changes as the
  number changes, so it's meant to be asked again later, not just once.
