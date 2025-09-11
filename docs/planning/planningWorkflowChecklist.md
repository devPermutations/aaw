# Planning Workflow Checklist

## Overview
This checklist tracks the completion status of all planning phase artifacts and ensures proper workflow progression through the agent ecosystem.

## Phase Status: PLANNING

### PM (Product Manager) - Phase 1
- [ ] **projectBrief.md** - Define project scope, objectives, and requirements
  - Business objectives clearly defined
  - Functional requirements documented
  - Non-functional requirements specified
  - Success criteria established
  - Constraints and assumptions documented

### Architect - Phase 2
- [ ] **architecture.md** - Define system architecture and design decisions
  - System overview completed
  - Component architecture defined
  - Data flow diagrams created
  - Security considerations addressed
  - Scalability design documented
  - Integration points identified

- [ ] **techStack.md** - Define technology choices and justifications
  - Programming languages selected
  - Frameworks and libraries chosen
  - Database technologies defined
  - Infrastructure components specified
  - Development tools selected
  - Rationale for each choice documented

- [ ] **implementationPatterns.md** - Define coding standards and patterns
  - Design patterns selected
  - Coding standards defined
  - Error handling patterns established
  - Security patterns documented
  - Performance patterns defined
  - Testing patterns specified

### Senior Dev - Phase 3
- [ ] **Spike Analysis** - Identify high-risk areas requiring research
  - Up to 5 risk areas identified
  - Research approach defined
  - Findings documented
  - Recommendations provided
  - Implementation considerations noted

- [ ] **Spike Documents** (if required)
  - [ ] `/docs/planning/additionalInformation/spike-*.md` documents created
  - [ ] Each spike contains problem statement, research, findings
  - [ ] Risk assessments completed
  - [ ] Implementation considerations documented

### EM (Engineering Manager) - Phase 4
- [ ] **epicsHighLevelDescription.md** - Define high-level epics
  - Epic overview completed
  - Epic list with IDs and descriptions
  - Priority and dependencies established
  - Estimated effort documented
  - Acceptance criteria defined

- [ ] **Detailed Epic Documents**
  - [ ] `/docs/development/epics/` folder created
  - [ ] Individual `epic-*.md` files created for each epic
  - [ ] Detailed requirements documented
  - [ ] User stories defined
  - [ ] Technical specifications completed
  - [ ] Dependencies mapped
  - [ ] Effort estimation completed

## Quality Gates

### Planning Phase Completion Criteria
- [ ] All artifacts created and reviewed
- [ ] Cross-references between artifacts validated
- [ ] Technical feasibility confirmed
- [ ] Risk assessment completed
- [ ] Development team alignment achieved

### Transition to Development
- [ ] All planning artifacts approved
- [ ] Epic breakdown completed
- [ ] Development team briefed
- [ ] Development environment prepared
- [ ] Initial development artifacts created

## Notes
- Each agent must update this checklist upon completion of their artifacts
- PM has final approval authority for planning phase completion
- Any blocking issues should be documented and escalated
- Checklist serves as audit trail for planning phase compliance

---

*Last Updated: Auto-generated from agent workflow*
*Next Phase: Development (Ready when all items above are completed)*
