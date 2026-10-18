# Body Weight Workout GPT

A no-equipment workout coach for ChatGPT and Codex. Tell it your goal and how much time you have, and add HRV, sleep, or other recovery data if you track them. It builds a bodyweight session that matches how recovered you are: lighter on a low-HRV morning, harder when you're fresh.

Each workout has a warm-up, a main block with sets, reps or time, and rest, an easier and a harder version of every move, and a cooldown. It always fits the time you gave. The tone is upbeat, with a little humor.

## Install

```
codex plugin marketplace add ericporres/plugins
codex plugin add bodyweight-workout@porres-plugins
```

The ZIP for hosts that take an upload is attached to each [release](https://github.com/ericporres/plugins/releases).

## Try it

- `High HRV day, what should I do?`
- `20 minutes in a hotel room, want endurance. HRV 48 (my baseline is 60), slept 6 hours.`

## Safety

This is coaching, not medical advice. Stop if you feel sharp pain, chest pain, or dizziness. If you're pregnant, recovering from surgery, or managing a heart condition or an injury, check with your clinician first.

## What it touches

Health data you type (HRV, sleep, weight) stays in your conversation with the host app. The plugin has no code and makes no network calls, and nothing reaches me. [Privacy policy](https://porres.com/plugins/privacy/) · [Support](https://porres.com/plugins/support/) · [Terms](https://porres.com/plugins/terms/)

MIT License (see the repository root). Built by [Eric Porres](https://porres.com).
