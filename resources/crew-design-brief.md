# CrewAI Design Brief

Complete this brief before implementing a multi-agent crew. Use it to test whether multiple agents are justified and to prevent overlapping roles.

## 1. Goal

- **Project name:**
- **Owner:**
- **Problem to solve:**
- **Final deliverable:**
- **Success criteria:**
- **Why multiple agents are necessary:**

## 2. Architecture Choice

- [ ] Single function or deterministic workflow is sufficient.
- [ ] Single agent is sufficient.
- [ ] Sequential Crew is appropriate.
- [ ] Hierarchical Crew is appropriate.
- [ ] Flow is required for state, events, or branching.
- [ ] Flow with one or more Crews is required.

**Reason for the selected architecture:**

## 3. Agent Responsibilities

| Agent | Role | Goal | Inputs | Outputs | Tools | Must not do |
|---|---|---|---|---|---|---|
| Agent 1 | | | | | | |
| Agent 2 | | | | | | |
| Agent 3 | | | | | | |

Each role should own a distinct responsibility. Avoid duplicate agents that perform the same reasoning without a clear review or validation purpose.

## 4. Task Plan

| Order | Task | Assigned agent | Context dependency | Expected output | Completion criteria |
|---:|---|---|---|---|---|
| 1 | | | | | |
| 2 | | | | | |
| 3 | | | | | |

## 5. Tools and Permissions

| Tool | Agent | Permission / scope | Input validation | Side effect |
|---|---|---|---|---|
| | | | | |

- **Credentials source:**
- **Human approval points:**
- **Timeouts and rate limits:**

## 6. Execution Controls

- **Process:** sequential / hierarchical / Flow
- **Max iterations:**
- **Rate limits:**
- **Memory requirement:**
- **Retry policy:**
- **Failure / escalation path:**

## 7. Acceptance Tests

- [ ] Each agent's task can be tested independently.
- [ ] Context reaches downstream tasks correctly.
- [ ] Final output satisfies acceptance criteria.
- [ ] Tool errors are handled.
- [ ] Iteration and rate limits are effective.
- [ ] Credentials are not exposed.
- [ ] The full crew is better than a simpler baseline.

## Approval

- **Designer:**
- **Reviewer:**
- **Date:**
- **Status:** draft / revise / approved
