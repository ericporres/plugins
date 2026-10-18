# GPT Prompt Builder

A plugin for ChatGPT and Codex that builds copy-and-paste prompts for any task.

You describe the job. It asks only for what's missing (three questions at most), then returns a self-contained prompt with a reasoning scaffold, a verification step, and a privacy check. It runs the prompt only after you approve it.

It started as a custom GPT. This is the same instruction set, packaged as a plugin.

## Install

**Claude Code**

```
claude plugin marketplace add ericporres/plugins
claude plugin install gpt-prompt-builder@porres-plugins
```

Then call it as `/gpt-prompt-builder:prompt-builder`, or just ask; Claude loads it when the request fits. **Claude Desktop:** add the marketplace `ericporres/plugins` in plugin settings and install from there.

**Codex CLI**

```
codex plugin marketplace add ericporres/plugins
codex plugin add gpt-prompt-builder@porres-plugins
```

**ChatGPT desktop app:** clone the repository and add it as a local marketplace.

**ZIP:** each [release](https://github.com/ericporres/plugins/releases) includes the plugin folder as a ZIP, for hosts that take an upload.

## Try it

- `ASSISTANT: Create a reusable prompt to triage my inbox and draft replies in my voice.`
- `CREATOR: Give me a prompt to outline and draft a 600-word blog post on [topic] in [brand voice].`
- `STRATEGIST: Produce a prompt to compare 3 options against criteria and recommend one.`

## What it returns

**Quick Build** (the default): the prompt in one copy-and-paste block, plus at most one caveat when an assumption could make it miss.

**Advanced Build** (ask for it): the prompt, why it works, two test inputs, conservative and exploratory variants, and a pass/fail check against your constraints that names the one remaining uncertainty.

Either way, it asks up to three questions when the request is too thin to build from, and it runs a prompt only after you approve it.

## What it touches

Nothing outside the conversation. The plugin is instructions only: no code, no MCP server, no network calls. It sends nothing to me. Details: [privacy policy](https://porres.com/plugins/privacy/).

## Credits

Inspired by Section School, Ethan Mollick, and Charles Duhigg.

## Support, privacy, terms

- Support: [porres.com/plugins/support](https://porres.com/plugins/support/) or open an issue
- Privacy: [porres.com/plugins/privacy](https://porres.com/plugins/privacy/)
- Terms: [porres.com/plugins/terms](https://porres.com/plugins/terms/)

MIT License (see the repository root). Built by [Eric Porres](https://porres.com).
