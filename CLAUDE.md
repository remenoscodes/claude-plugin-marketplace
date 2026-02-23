# claude-plugin-marketplace

Central marketplace for Claude Code plugins by Emerson Soares. Lists plugins via URL-based sources with CI validation.

Inherits workspace conventions from `~/CLAUDE.md`.

## Status
- **Version**: 1.0.0
- **State**: active
- **Deploy**: GitHub (`remenoscodes/claude-plugin-marketplace`), registered locally in `~/.claude/plugins/known_marketplaces.json`

## Stack
Claude Code marketplace format: JSON manifest (`.claude-plugin/marketplace.json`).
CI: GitHub Actions validation workflow.

## Key Commands
```bash
/plugin marketplace add remenoscodes/claude-plugin-marketplace   # Register marketplace
/plugin install claude-language-coach                             # Install a listed plugin
/plugin install claude-git-native-issue                           # Install a listed plugin
```

## Architecture
- `.claude-plugin/marketplace.json` — Plugin manifest listing all available plugins with URL-based sources
- Each plugin lives in its own repository; no submodules or local copies
- Plugins cached by commit hash in `~/.claude/plugins/cache/{marketplace}/{plugin}/{hash}/`
- CI workflow validates manifest structure on push/PR

## Related Projects
- `~/source/remenoscodes.claude-language-coach` — Listed plugin: ambient language coaching
- `~/source/remenoscodes.claude-git-native-issue` — Listed plugin: git-native issue tracking
