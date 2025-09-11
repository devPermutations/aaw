# Software Development Agent Ecosystem

A multi-agent system designed to streamline software development through collaborative AI agents across planning and development phases.

## Overview

This project implements an agent ecosystem that coordinates specialized AI agents to deliver software projects through planning to deployment. The system uses XML-based agent definitions and follows a structured workflow approach.

## Architecture

### Agent Organization

The system is organized into two primary workflow phases:

#### Planning Phase Agents (`.agents/planning/`)
- **PM (Product Manager)** - Requirements and roadmap planning
- **Architect** - System architecture and technical design
- **Spike** - Research and proof-of-concept development
- **EM (Engineering Manager)** - Team coordination and oversight
- **Release Manager** - Deployment and release coordination

#### Development Phase Agents (`.agents/development/`)
- **Git Handler** - Version control management
- **Developer** - Code implementation and development
- **Code Reviewer** - Code quality assurance
- **QA (Quality Assurance)** - Testing and validation

### Meta-Agent System

- **Agent Generator** (`.agents/agent_generator.md`) - Meta-agent for creating and managing other agents
- **Agent Template** (`.agents/agent_template.md`) - Standardized template for agent definitions

## Project Structure

```
.
├── .agents/                   # Agent definitions and templates
│   ├── agent_generator.md     # Meta-agent for creating agents
│   ├── agent_template.md      # Standardized agent template
│   ├── planning/              # Planning phase agents
        ├── pm.md              # Project manager
        ├── architect.md       # Architect
        ├── senior-dev.md      # Senior Developer
        └── em.md              # Engineering Manager                                 
│   └── development/           # Development phase agents
        ├── git-handler.md     # GitHub opperations (this agent is optional and not necesarily part of the workflow)
        ├── developer.md       # Developer
        ├── pr-reviewer.md     # Pull Request reviewer
        └── qa.md              # Quality Assurance Engineer                                
└── docs/                      # Documentation (artifacts go here)
```

## Getting Started

The workflows have strong dependencies and are best used as 
Planning Flow
PM > Architect > Senior Dev > EM . This flow produces the artifacts that the Development flow will need
Development Flow
Dev > PR Reviewer > QA

### Prerequisites

#### GitHub CLI (Strongly Recommended)
The agent ecosystem heavily utilizes GitHub CLI (`gh`) for version control operations, pull request management, and repository coordination. While not strictly required, it's strongly recommended for optimal functionality.

**gh Installation Instructions:**

**Windows:**
```powershell
# Using winget (recommended)
winget install --id GitHub.cli

# Or using Chocolatey
choco install gh

# Or using Scoop
scoop install gh
```

**macOS:**
```bash
# Using Homebrew (recommended)
brew install gh

# Or using MacPorts
sudo port install gh
```

**Linux:**
```bash
# Ubuntu/Debian
curl -fsSL https://cli.github.com/packages/githubcli-archive-keyring.gpg | sudo dd of=/usr/share/keyrings/githubcli-archive-keyring.gpg
echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/githubcli-archive-keyring.gpg] https://cli.github.com/packages stable main" | sudo tee /etc/apt/sources.list.d/github-cli.list > /dev/null
sudo apt update
sudo apt install gh

# CentOS/RHEL/Fedora
sudo dnf install 'dnf-command(config-manager)'
sudo dnf config-manager --add-repo https://cli.github.com/packages/rpm/gh-cli.repo
sudo dnf install gh

# Arch Linux
sudo pacman -S github-cli
```

**Post-Installation Setup:**
```bash
# Authenticate with GitHub
gh auth login

# Verify installation
gh --version
```



## License

[Add your license information here]

## Support

For questions about the agent ecosystem:
- Review the `agent_generator.md` for creation guidelines
- Check `agent_template.md` for structural requirements
- Refer to individual agent documentation for specific capabilities
- For GitHub CLI issues, see the Prerequisites section or visit [GitHub CLI Documentation](https://cli.github.com/manual/)

---

*This project represents a cutting-edge approach to AI-assisted software development through structured agent collaboration.*