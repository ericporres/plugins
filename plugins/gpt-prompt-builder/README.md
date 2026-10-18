# GPT Prompt Builder

A plugin for ChatGPT and Codex that builds copy-and-paste prompts for any task.

You describe the job. It asks only for what's missing (three questions at most), then returns a self-contained prompt with a reasoning scaffold, a verification step, and a privacy check. It runs the prompt only after you approve it.

It started as a custom GPT. This is the same instruction set, packaged as a plugin.

## Install

**Codex CLI**

```
codex plugin marketplace add ericporres/plugins
codex plugin add gpt-prompt-builder@porres-plugins
```

**ChatGPT desktop app:** clone this repository, then add the folder as a local marketplace. The app reads `.agents/plugins/marketplace.json` at the repository root.

**ZIP:** each [release](https://github.com/ericporres/plugins/releases) includes `gpt-prompt-builder.zip`, the plugin folder on its own, for hosts that take a ZIP upload.

## Try it

- `ASSISTANT: Create a reusable prompt to triage my inbox and draft replies in my voice.`
- `CREATOR: Give me a prompt to outline and draft a 600-word blog post on [topic] in [brand voice].`
- `STRATEGIST: Produce a prompt to compare 3 options against criteria and recommend one.`

## What it returns

1. A draft prompt in one copy-and-paste block: role and context, task and scope, inputs and assumptions, constraints, a reasoning scaffold, and the output format.
2. A short test against your goal, with the gaps it found.
3. A refined final prompt, plus variants when you ask for them.

It never asks the model to reveal private chain-of-thought. The prompts it writes ask for short reasoning summaries and labeled assumptions instead.

## What it touches

Nothing outside the conversation. The plugin is instructions only: no code, no MCP server, no network calls. It sends nothing to me. Details: [privacy policy](https://porres.com/plugins/privacy/).

## Credits

Inspired by Section School, Ethan Mollick, and Charles Duhigg.

## Support, privacy, terms

- Support: [porres.com/plugins/support](https://porres.com/plugins/support/) or open an issue
- Privacy: [porres.com/plugins/privacy](https://porres.com/plugins/privacy/)
- Terms: [porres.com/plugins/terms](https://porres.com/plugins/terms/)

MIT License (see the repository root). Built by [Eric Porres](https://porres.com).
