---
description: Check that each beat of a timed video script fits its seconds, and fix the overpacked ones.
argument-hint: "[script with timings]"
---

Load the `ad-creative-teardown:ad-creative-teardown` skill unless it is already loaded, then run its script timing check on:

$ARGUMENTS

Use a script already in this conversation if none is given here. Check every beat three ways:

1. Voice-over: count the spoken words. At about 2.5 words a second, a beat holds its seconds × 2.5, so about 7 words in 3 seconds.
2. On-screen text: it must stay up at least as long as it takes to say it aloud at the same pace. Text that says something different from the voice-over at the same moment competes with it.
3. Actions: a beat of about three seconds or less holds one action. Count the verbs in the shot description.

Deliver a beat table with a verdict for each beat, a fix for each flagged beat (cut words, split the beat or retime it, with the new word counts and timings), and the revised script with its total length. In the first three seconds, cut rather than extend.

Ask for at most one missing input. With no script, ask for it and stop. If the script has no timings, give each beat the time it needs and ask nothing.
