# remenoscodes — Claude Code Plugins

Central marketplace for Claude Code plugins by [Emerson Soares](https://github.com/remenoscodes).

## Plugins

| Plugin | Category | Description |
|--------|----------|-------------|
| [claude-language-coach](https://github.com/remenoscodes/claude-language-coach) | Learning | Ambient language coaching during coding sessions |
| [claude-git-native-issue](https://github.com/remenoscodes/claude-git-native-issue) | Productivity | Git-native issue tracking replacing Claude's internal task management |

## Installation

Add this marketplace to Claude Code:

```
/plugin marketplace add remenoscodes/claude-plugin-marketplace
```

Then install any plugin:

```
/plugin install claude-language-coach
/plugin install claude-git-native-issue
```

## Architecture

This marketplace uses URL-based plugin sources. Each plugin lives in its own repository and is fetched directly by Claude Code on install. No submodules, no local copies.
