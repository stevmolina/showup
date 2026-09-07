# Show Up

Show Up is an Agent Plugin for turning real work into personal social content. It provides four Agent Skills:

- `showup-capture` captures evidence and story material.
- `showup-draft` turns grounded material into voice-aware drafts for X and LinkedIn.
- `showup-publish` moves approved copy through Typefully.
- `showup-review` reviews results and improves the content system.

## Compatibility

The root `plugin.json` follows the [Agent Plugins 1.0.0 specification](https://agent-plugins.org/specification). Compatible clients, including Codex and Cursor, discover the skills in `skills/` automatically.

The `.codex-plugin/plugin.json` manifest is retained for Codex marketplace presentation metadata and compatibility with existing local installs.

## Install for local development

### Cursor

Link this repository into Cursor's local plugin directory, then reload the window:

```bash
mkdir -p ~/.cursor/plugins/local
ln -s /absolute/path/to/showup ~/.cursor/plugins/local/showup
```

Open **Customize** and confirm that the four Show Up skills appear.

### Codex

Add this repository as a marketplace from the Codex app or CLI:

```bash
codex plugin marketplace add stevmolina/showup --ref main
codex plugin add showup@showup
```

Restart the Codex app after adding or upgrading the marketplace, then start a new conversation so Codex loads the updated skills.

## Structure

```text
showup/
├── plugin.json
├── .agents/
│   └── plugins/
│       └── marketplace.json
├── .codex-plugin/
│   └── plugin.json
├── skills/
│   ├── showup-capture/
│   ├── showup-draft/
│   ├── showup-publish/
│   └── showup-review/
└── references/
```
