# claude-agents-crewai-skill

A Claude Code skill for designing and implementing multi-agent applications with CrewAI.

## Overview

CrewAI supports collaboration between specialized agents with defined roles, goals, tools, and tasks. This skill helps structure a crew, coordinate task execution, connect external capabilities, and use flows when a workflow needs explicit control.

The aim is to create the smallest useful team of agents, not the largest possible one.

## Main Capabilities

- Define agents with clear roles and responsibilities.
- Create tasks with expected outputs.
- Coordinate sequential and collaborative execution.
- Connect tools to agents.
- Design CrewAI Flows for structured workflows.
- Manage shared context and task dependencies.
- Diagnose common configuration and runtime problems.
- Evaluate the quality of the final crew output.

## When to Use It

Use this skill when a task benefits from multiple specialized agents, such as research followed by analysis and writing, or when a workflow needs role-based delegation and controlled execution.

For simple deterministic tasks, a regular function or single agent may be more reliable.

## Installation

Install the required CrewAI packages for the project, then clone the skill:

```bash
git clone https://github.com/Brajesh31/claude-agents-crewai-skill.git ~/.claude/skills/agents-crewai
```

## Usage

Invoke the skill for CrewAI design and implementation:

```text
/agents-crewai
```

Provide the overall goal, available tools, task dependencies, expected deliverables, and any approval requirements.

## Recommended Workflow

1. Define the final outcome and success criteria.
2. Identify distinct responsibilities that justify separate agents.
3. Create focused agent roles and goals.
4. Break the work into tasks with clear inputs and outputs.
5. Define task dependencies and execution order.
6. Add tools with narrow permissions.
7. Use a Flow when the process needs explicit branching or event handling.
8. Test with representative tasks.
9. Inspect intermediate outputs and final quality.
10. Refine roles only when evaluation shows a real need.

## Reference Guide

| File | Focus |
|---|---|
| `references/flows.md` | Structured workflow orchestration |
| `references/tools.md` | Agent tools and capabilities |
| `references/troubleshooting.md` | Setup and runtime troubleshooting |

## Multi-Agent Design Checklist

- Each agent has a distinct responsibility.
- Goals and expected outputs are explicit.
- Tasks have clear dependencies.
- Tools are limited to required operations.
- Shared state is controlled.
- Failures are surfaced and handled.
- Outputs are reviewed before downstream use.
- The crew is evaluated on task quality, not agent count.

## Repository Contents

- `SKILL.md`: Main CrewAI skill instructions.
- `references/`: Flows, tools, and troubleshooting guidance.
- `README.md`: Setup and multi-agent workflow.

## Practical Principle

Additional agents introduce coordination cost and more failure points. Start with a small crew, measure the result, and add roles only when specialization improves the outcome.
