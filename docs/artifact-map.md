# Software Development Agent Ecosystem - Artifact Map

## Overview

This document defines the complete artifact structure for the software development workflow, mapping each artifact to its responsible agent, dependencies, and workflow progression. The system follows a linear dependency chain ensuring proper information flow between planning and development phases.

## Directory Structure

```
docs/
├── artifact-map.md                 # This document
├── planning/
│   ├── planningWorkflowChecklist.md
│   ├── projectBrief.md
│   ├── architecture.md
│   ├── techStack.md
│   ├── implementationPatterns.md
│   └── additionalInformation/      # Spike documents
│       ├── spike-database-design.md
│       ├── spike-api-performance.md
│       └── ...
└── development/
    ├── epicsHighLevelDescription.md
    ├── epics/                      # Detailed epic documents
    │   ├── epic-user-authentication.md
    │   ├── epic-payment-processing.md
    │   └── ...
    ├── functionMap.md
    ├── testStrategy.md
    └── conversations/               # Epic conversations
        ├── epic-user-authentication-conversation.md
        ├── epic-payment-processing-conversation.md
        └── ...
```

## Workflow Phases

### Phase 1: Planning
**Purpose**: Define project scope, technical architecture, and identify risks
**Agents**: PM → Architect → Senior Dev → EM
**Flow**: Linear with dependencies

### Phase 2: Development
**Purpose**: Execute development work with quality assurance
**Agents**: EM → Developer → PR Reviewer → QA
**Flow**: Parallel per-epic with coordination

---

## Artifact Definitions

### 1. Planning Workflow Checklist
**File**: `docs/planning/planningWorkflowChecklist.md`
**Responsible Agent**: Auto-generated/Maintained by all agents
**Purpose**: Track completion status of planning phase tasks
**Format**:
```
Planning Checklist
PM: ✅ complete artifactLink
Architect: ✅ complete artifactLink
Senior Dev: ✅ complete artifactLink (optional spikes)
EM: ✅ complete artifactLink
```

### 2. Project Brief
**File**: `docs/planning/projectBrief.md`
**Responsible Agent**: PM (Product Manager)
**Purpose**: Define project scope, objectives, and requirements
**Dependencies**: None (initial artifact)
**Consumers**: Architect, Senior Dev, EM
**Content Structure**:
- Project Overview
- Business Objectives
- Functional Requirements
- Non-functional Requirements
- Success Criteria
- Constraints and Assumptions

### 3. Architecture Document
**File**: `docs/planning/architecture.md`
**Responsible Agent**: Architect
**Purpose**: Define system architecture and design decisions
**Dependencies**:
- `docs/planning/projectBrief.md`
**Consumers**: Senior Dev, EM, Developer
**Content Structure**:
- System Overview
- Component Architecture
- Data Flow Diagrams
- Security Considerations
- Scalability Design
- Integration Points

### 4. Technology Stack
**File**: `docs/planning/techStack.md`
**Responsible Agent**: Architect
**Purpose**: Define technology choices and justifications
**Dependencies**:
- `docs/planning/projectBrief.md`
- `docs/planning/architecture.md`
**Consumers**: Senior Dev, EM, Developer, QA
**Content Structure**:
- Programming Languages
- Frameworks and Libraries
- Database Technologies
- Infrastructure Components
- Development Tools
- Rationale for Each Choice

### 5. Implementation Patterns
**File**: `docs/planning/implementationPatterns.md`
**Responsible Agent**: Architect
**Purpose**: Define coding standards and architectural patterns
**Dependencies**:
- `docs/planning/projectBrief.md`
- `docs/planning/architecture.md`
- `docs/planning/techStack.md`
**Consumers**: Senior Dev, Developer, PR Reviewer
**Content Structure**:
- Design Patterns
- Coding Standards
- Error Handling Patterns
- Security Patterns
- Performance Patterns
- Testing Patterns

### 6. Spike Documents
**Files**: `docs/planning/additionalInformation/spike-*.md`
**Responsible Agent**: Senior Dev
**Purpose**: Research high-risk areas requiring more information
**Dependencies**:
- `docs/planning/projectBrief.md`
- `docs/planning/architecture.md`
- `docs/planning/techStack.md`
- `docs/planning/implementationPatterns.md`
**Consumers**: EM, Developer
**Selection Criteria**: Up to 5 areas of highest technical risk
**Content Structure** (per spike):
- Problem Statement
- Research Approach
- Findings and Recommendations
- Implementation Considerations
- Risk Assessment

### 7. Epics High-Level Description
**File**: `docs/development/epicsHighLevelDescription.md`
**Responsible Agent**: EM (Engineering Manager)
**Purpose**: Define high-level epics for development execution
**Dependencies**:
- All planning artifacts
- Spike documents (if any)
**Consumers**: Developer, PR Reviewer, QA
**Content Structure**:
- Epic Overview
- Epic List with IDs and short descriptions
- Priority and Dependencies
- Estimated Effort
- Acceptance Criteria

### 8. Detailed Epic Documents
**Files**: `docs/development/epics/epic-*.md`
**Responsible Agent**: EM (Engineering Manager)
**Purpose**: Provide detailed specifications for each epic
**Dependencies**:
- `docs/development/epicsHighLevelDescription.md`
- All planning artifacts
**Consumers**: Developer, PR Reviewer, QA
**Content Structure** (per epic):
- Epic Overview
- Detailed Requirements
- User Stories
- Acceptance Criteria
- Technical Specifications
- Dependencies
- Effort Estimation

### 9. Epic Conversation Documents
**Files**: `docs/development/conversations/epic-*-conversation.md`
**Responsible Agent**: All development agents (Developer, PR Reviewer, QA)
**Purpose**: Track development progress and feedback per epic
**Dependencies**:
- `docs/development/epics/epic-*.md`
**Consumers**: All development agents
**Format**:
```
Epic Conversation
Dev: ✅ complete, PR #123
PR Reviewer: ✅ PR feedback - approved with minor suggestions
QA: ✅ QA test link - test-results/epic-user-auth-2024-01-15.md
```

### 10. Function Map
**File**: `docs/development/functionMap.md`
**Responsible Agent**: PR Reviewer
**Purpose**: Comprehensive documentation of all functions to prevent duplication
**Dependencies**:
- All PR reviews
**Consumers**: Developer, PR Reviewer, QA
**Content Structure**:
- File Path
- Function Name
- Parameters
- Return Type
- Short Description (10-12 words)
- Last Updated
- Associated Epic

### 11. Test Strategy
**File**: `docs/development/testStrategy.md`
**Responsible Agent**: QA
**Purpose**: Define testing framework and comprehensive test coverage
**Dependencies**:
- `docs/development/epicsHighLevelDescription.md`
- All epic documents
**Consumers**: Developer, PR Reviewer, QA
**Content Structure**:
- Testing Framework
- Test Types (Unit, Integration, E2E)
- Test Environment Setup
- Test Data Management
- Coverage Requirements
- Automation Strategy
- Performance Testing
- Security Testing

---

## Agent Responsibilities Matrix

| Artifact | Creation Agent | Maintenance Agent | Dependencies |
|----------|----------------|-------------------|-------------|
| planningWorkflowChecklist.md | Auto-generated | All Planning Agents | None |
| projectBrief.md | PM | PM | None |
| architecture.md | Architect | Architect | projectBrief.md |
| techStack.md | Architect | Architect | projectBrief.md, architecture.md |
| implementationPatterns.md | Architect | Architect | All planning docs |
| Spike Documents | Senior Dev | Senior Dev | All planning docs |
| epicsHighLevelDescription.md | EM | EM | All planning docs + spikes |
| Detailed Epic Documents | EM | EM | epicsHighLevelDescription.md |
| Epic Conversations | All Dev Agents | All Dev Agents | Epic documents |
| functionMap.md | PR Reviewer | PR Reviewer | All PR reviews |
| testStrategy.md | QA | QA | Epic documents |

---

## Workflow Dependencies

### Linear Planning Flow:
1. **PM** → projectBrief.md
2. **Architect** → architecture.md, techStack.md, implementationPatterns.md
3. **Senior Dev** → Spike documents (optional)
4. **EM** → epicsHighLevelDescription.md, Detailed Epic Documents

### Parallel Development Flow (per Epic):
1. **EM** → Epic specifications
2. **Developer** → Code implementation (tracked in Epic Conversation)
3. **PR Reviewer** → Code review, functionMap.md updates
4. **QA** → Testing, testStrategy.md maintenance

---

## Quality Gates

### Planning Phase:
- **PM Checkpoint**: projectBrief.md completeness
- **Architect Checkpoint**: Technical documentation review
- **Senior Dev Checkpoint**: Spike completion (if required)
- **EM Checkpoint**: Epic definition completeness

### Development Phase:
- **Developer Checkpoint**: Code implementation completeness
- **PR Reviewer Checkpoint**: Code quality and function duplication check
- **QA Checkpoint**: Test coverage and quality assurance

---

## File Naming Conventions

- **Planning Documents**: lowercase-with-hyphens.md
- **Epic Documents**: epic-descriptive-name.md
- **Spike Documents**: spike-descriptive-topic.md
- **Conversation Documents**: epic-name-conversation.md
- **Folders**: lowercase-with-hyphens/

---

## Version Control Strategy

- All artifacts tracked in Git
- Semantic versioning for major releases
- Branch strategy: main, develop, feature/, release/, hotfix/
- PR reviews required for all artifact changes
- Automated artifact validation where possible

---

## Maintenance Guidelines

- **Regular Updates**: Artifacts updated as work progresses
- **Version History**: Git history tracks all changes
- **Cross-References**: Links between related artifacts
- **Review Process**: All artifact changes go through PR review
- **Backup Strategy**: Git provides complete artifact history

This artifact map serves as the foundation for creating accurate agent definitions that understand their responsibilities, dependencies, and integration points within the software development workflow.
