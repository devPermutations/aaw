# Software Development Agent Ecosystem

An intelligent multi-agent system designed to streamline software development through collaborative AI agents across planning and development phases.

## Overview

This project implements a sophisticated agent ecosystem that coordinates specialized AI agents to deliver software projects from concept to deployment. The system uses XML-based agent definitions and follows a structured workflow approach.

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

## Key Features

- **XML-Based Agent Definitions** - Structured, machine-readable agent specifications
- **Workflow Orchestration** - Seamless coordination between planning and development phases
- **Artifact-Driven Architecture** - Standardized inputs and outputs between agents
- **Quality Assurance Framework** - Built-in validation and review processes
- **GitHub CLI Integration** - Advanced version control and pull request management
- **Version Control Integration** - Git-aware agent operations
- **Iterative Refinement** - Continuous improvement through feedback loops

## Project Structure

```
.
├── .agents/                    # Agent definitions and templates
│   ├── agent_generator.md     # Meta-agent for creating agents
│   ├── agent_template.md      # Standardized agent template
│   ├── planning/              # Planning phase agents
│   └── development/           # Development phase agents
├── .gitignore                # Git ignore rules
├── README.md                 # This file
└── docs/                     # Documentation (to be created)
```

## Getting Started

### Prerequisites

#### GitHub CLI (Strongly Recommended)
The agent ecosystem heavily utilizes GitHub CLI (`gh`) for version control operations, pull request management, and repository coordination. While not strictly required, it's strongly recommended for optimal functionality.

**Installation Instructions:**

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

1. **Initialize the Agent Ecosystem**
   ```bash
   # Review the meta-agent system
   cat .agents/agent_generator.md
   cat .agents/agent_template.md
   ```

2. **Create Your First Agent**
   - Use the `agent_generator.md` to create new agents
   - Follow the XML template structure from `agent_template.md`
   - Place agents in appropriate phase directories

3. **Configure Workflows**
   - Define artifact mappings and dependencies
   - Set up coordination protocols between agents
   - Configure quality gates and validation steps

## Agent Development Guidelines

### Creating New Agents
1. Start with the `agent_template.md` structure
2. Define clear roles and responsibilities
3. Specify input/output artifacts
4. Include quality standards and validation procedures
5. Add integration points with upstream/downstream agents

### Quality Standards
- All agents must include comprehensive meta information
- Clear artifact specifications with file paths
- Defined progress tracking mechanisms
- Error handling and escalation procedures
- Professional communication style guidelines

### Best Practices
- Use semantic versioning for agent updates
- Maintain consistent XML structure across all agents
- Document dependencies and integration points
- Include comprehensive error handling
- Follow established naming conventions

## Workflow Integration

### Planning → Development Handoff
1. Planning agents produce comprehensive documentation
2. Development agents consume planning artifacts
3. Quality gates ensure requirements are met
4. Progress tracking maintains transparency

### Continuous Coordination
- Real-time progress updates between phases
- Artifact validation at each stage
- Escalation paths for blocked work
- Iterative refinement based on feedback

## Documentation

- **Agent Specifications**: Each agent includes comprehensive documentation
- **Workflow Patterns**: Standardized approaches for common scenarios
- **Quality Standards**: Validation criteria and review processes
- **Integration Guides**: How agents coordinate with each other

## Contributing

1. Follow the established agent template structure
2. Include comprehensive documentation
3. Add appropriate quality checks and validation
4. Update integration points when modifying agent relationships
5. Maintain consistency with existing patterns

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