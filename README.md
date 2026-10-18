# Plugins by Eric Porres

Plugins I build for my own work and publish for Claude, ChatGPT, and Codex. Each lives in its own folder under `plugins/`. This repository is also a plugin marketplace for both Claude and Codex, so one command adds all of them.

| Plugin | What it does | Type |
|---|---|---|
| [GPT Prompt Builder](plugins/gpt-prompt-builder/) | Builds copy-and-paste prompts with a reasoning scaffold, a verification step, and a privacy check | Skills only |
| [Trippin' The Chat Fantastic](plugins/trippin-the-chat-fantastic/) | Brainstorms 13 wild ideas when you say "open the portal," then picks the two that could work | Skills only |
| [Body Weight Workout GPT](plugins/bodyweight-workout/) | Bodyweight-only workouts matched to your goal, your time, and your recovery (HRV, sleep) | Skills only |

## Install

**Claude Code**

```
claude plugin marketplace add ericporres/plugins
claude plugin install gpt-prompt-builder@porres-plugins
claude plugin install trippin-the-chat-fantastic@porres-plugins
claude plugin install bodyweight-workout@porres-plugins
```

Or from inside a session: `/plugin marketplace add ericporres/plugins`, then `/plugin` to browse. `claude plugin marketplace update porres-plugins` pulls new versions.

**Claude Desktop:** in plugin settings, add a marketplace from GitHub, enter `ericporres/plugins`, then install the plugins you want.

**Codex CLI**

```
codex plugin marketplace add ericporres/plugins
codex plugin add gpt-prompt-builder@porres-plugins
codex plugin add trippin-the-chat-fantastic@porres-plugins
codex plugin add bodyweight-workout@porres-plugins
```

`codex plugin marketplace upgrade porres-plugins` pulls new versions.

**ChatGPT desktop app:** clone this repository and add the folder as a local marketplace. The app reads `.agents/plugins/marketplace.json` at the root.

**ZIP:** each [release](https://github.com/ericporres/plugins/releases) attaches one plugin folder as a ZIP, for hosts that take an upload.

## Layout

```
.claude-plugin/marketplace.json    Claude marketplace
.agents/plugins/marketplace.json   Codex and ChatGPT marketplace
plugins/<name>/
  plugin.json                      Agent Plugins manifest (Codex, ChatGPT)
  skills/<skill>/SKILL.md          instructions the model loads (Agent Skills, read by every host)
  assets/                          icon
  README.md                        what it does, how to use it
```

The plugins follow the [Agent Plugins](https://agent-plugins.org/) layout. Claude doesn't read that manifest yet. It reads `skills/` directly and takes the name, description, and version from `.claude-plugin/marketplace.json`.

## Support, privacy, terms

- Support: [porres.com/plugins/support](https://porres.com/plugins/support/) or open an issue
- Privacy: [porres.com/plugins/privacy](https://porres.com/plugins/privacy/)
- Terms: [porres.com/plugins/terms](https://porres.com/plugins/terms/)

MIT License. Personal projects, not products of my employer.
