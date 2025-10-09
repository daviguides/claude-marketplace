# Contributing to Davi Guides Marketplace

Thank you for your interest in contributing to this Claude Code plugin marketplace!

## Adding a New Plugin

### Requirements

Your plugin must:
1. Be hosted on GitHub (or another Git platform)
2. Have a valid `.claude-plugin/plugin.json` file
3. Follow Claude Code plugin structure guidelines
4. Be properly documented

### Plugin Structure

Ensure your plugin repository has this structure:

```
your-plugin/
├── .claude-plugin/
│   └── plugin.json          # Required: Plugin metadata
├── commands/                 # Optional: Custom slash commands
├── agents/                   # Optional: Custom agents
├── hooks/                    # Optional: Event handlers
├── README.md                # Required: Documentation
└── LICENSE                  # Recommended: License file
```

### Submission Process

1. **Fork this repository**

2. **Add your plugin to `marketplace.json`:**
   ```json
   {
     "name": "your-plugin-name",
     "source": {
       "source": "github",
       "repo": "your-username/your-plugin-repo"
     },
     "description": "Brief description of your plugin"
   }
   ```

3. **Update documentation:**
   - Add entry to `README.md` (Available Plugins section)
   - Add detailed information to `PLUGINS.md`

4. **Submit Pull Request:**
   - Clear title: "Add [plugin-name] plugin"
   - Description explaining what your plugin does
   - Link to plugin repository
   - Any special installation or usage notes

### Plugin Naming Conventions

- Use **kebab-case** for plugin names
- Be descriptive and specific
- Avoid generic names like "utils" or "tools"

**Good examples:**
- `semantic-docstrings`
- `code-zen`
- `python-test-helpers`

**Bad examples:**
- `utils`
- `helper`
- `my_plugin`

### Plugin Description Guidelines

- Keep it concise (one sentence)
- Explain **what** the plugin does
- Highlight main use case

**Good example:**
```
"Enhanced code documentation with semantic docstring support"
```

**Bad example:**
```
"A plugin that helps with stuff"
```

## Quality Standards

### Required
- [ ] Valid `plugin.json` with name, version, description
- [ ] README.md with clear usage instructions
- [ ] Plugin follows Claude Code plugin guidelines
- [ ] Repository is publicly accessible

### Recommended
- [ ] LICENSE file
- [ ] CHANGELOG.md
- [ ] Examples or demos
- [ ] Tests (if applicable)

## Review Process

1. **Automated checks:** Ensure marketplace.json is valid
2. **Manual review:** Plugin quality and documentation
3. **Testing:** Verify plugin installs and works correctly
4. **Approval:** Merge PR and publish

## Questions?

Open an issue in this repository if you have any questions about contributing.

## Code of Conduct

- Be respectful and constructive
- Follow plugin naming and documentation guidelines
- Ensure your plugin adds value to the marketplace
- Maintain your plugin and respond to issues
