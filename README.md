# Show Up

Show Up is an Agent Plugin for turning real work into personal social content. It provides four Agent Skills:

- `showup-capture` captures evidence and story material.
- `showup-draft` turns grounded material into voice-aware drafts for X and LinkedIn.
- `showup-publish` moves approved copy through Typefully.
- `showup-review` reviews results and improves the content system.

## Which plugin owns what

Show Up sits next to Social Media Studio in Steven's setup. To keep agents from picking the wrong one:

- **Social Media Studio** owns writing a new post from work ("turn today's work into an X post").
- **Show Up** owns capture of proof into the Content Inbox (`showup-capture`), drafting from a saved inbox entry, a quote-post or an adaptation (`showup-draft`), the weekly review (`showup-review`) and publishing (`showup-publish`, typed only).

## Compatibility

The root `plugin.json` follows the [Agent Plugins 1.0.0 specification](https://agent-plugins.org/specification). Compatible clients, including Codex and Cursor, discover the skills in `skills/` automatically.

The `.codex-plugin/plugin.json` manifest is retained for Codex marketplace presentation metadata and compatibility with existing local installs.

Claude Code reads `.claude-plugin/plugin.json`, and `.claude-plugin/marketplace.json` makes this repository its own one-plugin marketplace.

`showup-publish` posts publicly, so it only runs when typed as a command (`/showup:showup-publish`); agents never start it on their own.

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

### Claude Code

```bash
claude plugin marketplace add stevmolina/showup
claude plugin install showup@showup
```

Start a new session after installing or updating (`claude plugin marketplace update showup`).

## Structure

```text
showup/
├── plugin.json
├── .claude-plugin/
│   ├── plugin.json
│   └── marketplace.json
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
