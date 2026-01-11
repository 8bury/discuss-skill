# Discuss Skill for Claude Code

A Claude Code skill that conducts in-depth technical interviews about features and tasks, then generates comprehensive specification documents.

## Overview

The `/discuss` skill transforms vague feature ideas into detailed, actionable specifications through an iterative interview process. Instead of writing specs yourself, Claude asks targeted, deep questions about technical implementation, UI/UX, trade-offs, and edge cases—then compiles everything into a well-structured specification document.

## Features

- **In-depth interviews**: Uses `AskUserQuestion` to probe technical details, architectural decisions, and implementation concerns
- **Iterative questioning**: Builds on previous answers to go deeper rather than staying surface-level
- **Non-obvious insights**: Asks about edge cases, failure modes, monitoring, and other often-overlooked aspects
- **Automatic spec generation**: Creates a comprehensive markdown specification file with a relevant filename
- **Flexible structure**: Adapts the spec document to match what was actually discussed

## Installation

### Option 1: Local Installation (for personal use)

1. Clone this repository:
```bash
cd ~/.claude/skills
git clone https://github.com/8bury/discuss-skill.git
```

2. Restart Claude Code or reload skills

### Option 2: Plugin Installation (for team sharing)

1. Add to your Claude Code plugins directory:
```bash
cd ~/.claude/plugins/marketplaces
git clone https://github.com/8bury/discuss-skill.git
```

2. Install the plugin:
```bash
/plugin install discuss-skill
```

## Usage

1. Start the discussion workflow:
```
/discuss
```

2. Describe your feature or task when prompted

3. Answer the in-depth questions Claude asks

4. Continue the interview until you've covered everything

5. Claude will generate a comprehensive spec document automatically

## Example Workflow

```
User: /discuss

Claude: Let me help you develop a comprehensive specification.
Please describe the task or feature you'd like to discuss in detail.

User: I want to add a real-time collaborative editing feature to our app

Claude: [Asks questions about:]
- WebSocket vs WebRTC vs operational transformation
- Conflict resolution strategies
- Presence indicators and cursor positions
- Offline editing and sync
- Performance with many concurrent users
- Security and authorization
- ...

[Multiple rounds of deep questioning]

Claude: I've created a comprehensive specification document at:
real-time-collaborative-editing-spec.md
```

## What Makes This Different

- **Goes deep**: Asks about failure modes, monitoring, rollback strategies—not just "what should it do?"
- **Challenges assumptions**: Respectfully probes decisions to ensure they're well-considered
- **Comprehensive coverage**: Technical, UX, security, performance, testing, deployment
- **Saves time**: No more staring at blank spec documents

## Specification Structure

Generated specs include:
- Overview & objectives
- User stories and use cases
- Technical requirements (architecture, tech stack, data model, APIs)
- UI/UX requirements (flows, design, accessibility)
- Non-functional requirements (performance, security, scalability)
- Edge cases & error handling
- Testing strategy
- Deployment plan
- Risks & mitigation
- Success criteria

## Requirements

- Claude Code (version 2.0+)
- No additional dependencies

## Credits

- **Created by**: [8bury](https://github.com/8bury)
- **Inspired by**: [@filippkowalski on X](https://x.com/filippkowalski) for the original idea of using in-depth interviews to generate specifications

## License

MIT License - see LICENSE file for details

## Contributing

Contributions welcome! Please open an issue or PR if you have suggestions for:
- Additional question categories
- Better spec templates
- Interview workflow improvements
- Documentation enhancements

## Support

- **Issues**: [GitHub Issues](https://github.com/8bury/discuss-skill/issues)
- **Discussions**: [GitHub Discussions](https://github.com/8bury/discuss-skill/discussions)

---

Made with ❤️ for better specification workflows
