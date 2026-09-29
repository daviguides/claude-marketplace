# Available Plugins

## Semantic Docstrings

### Description
Enhanced code documentation plugin that provides semantic docstring support for Python projects. Helps maintain consistent and meaningful documentation across your codebase.

### Features
- Semantic docstring templates
- Documentation best practices
- Automated documentation helpers

### Installation
```bash
/plugin install semantic-docstrings@daviguides-marketplace
```

### Repository
[github.com/daviguides/semantic-docstrings](https://github.com/daviguides/semantic-docstrings)

### Usage
After installation, the plugin provides custom commands and agents for documentation tasks.

---

## Code Zen

### Description
Python development plugin based on the Zen of Python principles. Enforces best practices, coding standards, and Pythonic patterns in your development workflow.

### Features
- Zen of Python guideline enforcement
- Code quality checks
- Best practices recommendations
- Python-specific development helpers

### Installation
```bash
/plugin install code-zen@daviguides-marketplace
```

### Repository
[github.com/daviguides/code-zen](https://github.com/daviguides/code-zen)

### Usage
After installation, the plugin provides custom commands and agents focused on Python best practices and code quality.

---

## Pragma

### Description
Operational discipline for Claude Code. Eliminates recurring operational mistakes: wrong agent types, lost context in delegation, AI tells in drafts, misuse of memory, and wasted user attention.

### Principles
- Delegation: right agent type, full context transfer, file isolation
- Communication: no AI tells (no em-dash), user decisions only, Slack-ready HTML
- Persistence: project knowledge base, not Claude memory
- Anti-Waste: always recommend, execute don't narrate
- User Idiom: reading conversational habits correctly

### Installation
```bash
/plugin install pragma@daviguides
```

### Repository
[github.com/daviguides/pragma](https://github.com/daviguides/pragma)

### Usage
Load with `/pragma:load` or include in system prompt via `gradient compile pragma`.

---

## Memo

### Description
Session artifact management for Claude Code. Handles session logs, standing contexts, handoff prompts, and meta-session coordination.

### Artifacts
- Session logs: structured record with metadata header and standard sections
- Contexts: durable insights that outlive sessions (methods, decisions with evidence)
- Next-session prompts: handoff with rational, pending tasks, @paths
- Meta-session prompts: coordinator role for non-implementing strategic sessions

### Installation
```bash
/plugin install memo@daviguides
```

### Repository
[github.com/daviguides/memo](https://github.com/daviguides/memo)

### Usage
Skills: `/memo:save-log`, `/memo:read-previous`, `/memo:handoff`, `/memo:save-context`. Load specs with `/memo:load`.

---

## Plugin Management

### List installed plugins
```bash
/plugin
```
Select "Manage Plugins" from the menu

### Enable/Disable plugins
```bash
/plugin enable plugin-name@daviguides-marketplace
/plugin disable plugin-name@daviguides-marketplace
```

### Uninstall plugins
```bash
/plugin uninstall plugin-name@daviguides-marketplace
```

### Update plugins
Plugins are automatically updated when the marketplace references are refreshed.
