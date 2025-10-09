# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Repository Overview

This is a Claude Code marketplace repository that hosts and distributes plugins for Claude Code. The marketplace focuses on Python development best practices, documentation tools, and coding standards enforcement.

**Core Structure:**
- `.claude-plugin/marketplace.json` - Marketplace configuration defining available plugins
- Plugin references point to external GitHub repositories (not hosted in this repo)
- Documentation files explain plugin capabilities and contribution guidelines

## Marketplace Architecture

### Plugin Registry System
The marketplace operates as a **registry/catalog** rather than a plugin host:
- Plugins are **referenced** via GitHub repositories in `marketplace.json`
- Each plugin entry contains: name, source repository, and description
- Users install plugins from their source repositories through this marketplace

### marketplace.json Structure
```json
{
  "name": "daviguides-marketplace",
  "owner": { "name": "...", "email": "..." },
  "plugins": [
    {
      "name": "plugin-name",
      "source": {
        "source": "github",
        "repo": "owner/repo"
      },
      "description": "Brief description"
    }
  ]
}
```

## Adding New Plugins

### Required Changes (3-file update pattern)
When adding a plugin, update ALL three files:

1. **`.claude-plugin/marketplace.json`** - Add plugin entry to `plugins` array
2. **`README.md`** - Add to "Available Plugins" section with install command
3. **`PLUGINS.md`** - Add detailed plugin documentation section

### Plugin Entry Requirements
- **Name:** kebab-case, descriptive (not generic)
- **Source:** GitHub repository with valid `.claude-plugin/plugin.json`
- **Description:** One clear sentence explaining purpose

### Validation Checklist
Before committing plugin additions:
- [ ] Plugin repository is publicly accessible
- [ ] Plugin has valid `.claude-plugin/plugin.json` file
- [ ] All three documentation files are updated consistently
- [ ] Plugin name follows kebab-case convention
- [ ] Description is concise and clear

## Repository Constraints

**This repo does NOT contain:**
- Plugin implementation code (lives in external repos)
- Custom slash commands or agents
- Python source code or tests

**This repo ONLY contains:**
- Marketplace metadata configuration
- Documentation and contribution guidelines
- License information

## Git Workflow

### Commit Message Pattern
Since changes typically involve registry updates:
- `feat(plugin): add [plugin-name] to marketplace` - New plugin
- `docs: update [plugin-name] documentation` - Doc changes
- `fix(marketplace): correct [plugin-name] repository URL` - Fixes

### Modified Files Pattern
Typical change involves modifying:
- `.claude-plugin/marketplace.json` (modified)
- `README.md` (modified)
- `PLUGINS.md` (modified)

## Installation Commands

Users interact with this marketplace through Claude Code commands:

```bash
# Add marketplace
/plugin marketplace add daviguides/claude-marketplace

# Install plugin from this marketplace
/plugin install plugin-name@daviguides-marketplace

# Browse available plugins
/plugin
```

## Quality Standards for Plugin Acceptance

As documented in CONTRIBUTING.md:
- Valid plugin.json in source repository
- Clear README with usage instructions
- Follows Claude Code plugin structure guidelines
- Publicly accessible repository
- Descriptive plugin name and description
