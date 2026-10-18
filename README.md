# Plugins by Eric Porres

Plugins I build for my own work and publish for ChatGPT and Codex. Each lives in its own folder under `plugins/`. This repository is also a plugin marketplace, so one command adds all of them.

| Plugin | What it does | Type |
|---|---|---|
| [GPT Prompt Builder](plugins/gpt-prompt-builder/) | Builds copy-and-paste prompts with a reasoning scaffold, a verification step, and a privacy check | Skills only |

## Install

**Codex CLI**

```
codex plugin marketplace add ericporres/plugins
codex plugin add gpt-prompt-builder@porres-plugins
```

`codex plugin marketplace upgrade porres-plugins` pulls new versions.

**ChatGPT desktop app:** clone this repository and add the folder as a local marketplace. The app reads `.agents/plugins/marketplace.json` at the root.

**ZIP:** each [release](https://github.com/ericporres/plugins/releases) attaches one plugin folder as a ZIP, for hosts that take an upload.

## Layout

```
.agents/plugins/marketplace.json   the marketplace: one entry per plugin
plugins/<name>/
  plugin.json                      manifest
  skills/                          instructions the model loads
  assets/                          icon
  README.md                        what it does, how to use it
```

## Support, privacy, terms

- Support: [porres.com/plugins/support](https://porres.com/plugins/support/) or open an issue
- Privacy: [porres.com/plugins/privacy](https://porres.com/plugins/privacy/)
- Terms: [porres.com/plugins/terms](https://porres.com/plugins/terms/)

MIT License. Personal projects, not products of my employer.
