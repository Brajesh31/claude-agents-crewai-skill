# CrewAI Multi-Agent Orchestration Skill

A Claude Code skill for designing and implementing multi-agent applications with CrewAI. It covers role-based agents, tasks, sequential and hierarchical processes, tools, memory, and event-driven Flows.

The focus is useful collaboration, not agent count. A small set of clearly scoped agents is usually easier to control, evaluate, and maintain than a large crew with overlapping responsibilities.

## What This Skill Covers

- Define agents with focused roles, goals, and backstories.
- Create tasks with explicit inputs and expected outputs.
- Pass context between dependent tasks.
- Orchestrate sequential and hierarchical processes.
- Use Flows for explicit state, events, and conditional routing.
- Connect built-in and custom tools.
- Configure memory and model providers.
- Diagnose installation, execution, tool, and state issues.
- Inspect task outputs and token usage.

## When to Use It

Use CrewAI when a problem benefits from multiple specialized agents collaborating on a defined outcome, such as research followed by analysis and report writing, or a workflow where a manager delegates to specialist roles.

A direct function, deterministic pipeline, or single agent is often the better choice for simple tasks. Multi-agent execution adds latency, cost, coordination overhead, and failure modes. Do not add agents unless specialization or delegation improves the result.

## Installation

The skill instructions document installing CrewAI:

~~~bash
python -m pip install crewai
~~~

For the additional tool collection, the skill documents:

~~~bash
python -m pip install 'crewai[tools]'
~~~

The skill repository itself can be installed into Claude Code:

~~~bash
git clone https://github.com/Brajesh31/claude-agents-crewai-skill.git ~/.claude/skills/agents-crewai
~~~

CrewAI packages and APIs evolve. Verify the current Python version requirements and package installation instructions against the official documentation before starting a new project.

## Usage

Invoke the skill in Claude Code:

~~~text
/agents-crewai
~~~

Provide the overall goal, input data, task dependencies, available tools, required outputs, and any approval or safety constraints.

## Core Concepts

### Agents

Agents represent specialized workers. Define a role, a goal, and enough backstory to guide behavior. Assign only the tools and permissions required for that role.

### Tasks

Tasks define work units. Their descriptions should identify the required operation, while `expected_output` should make completion observable. Use context dependencies when a downstream task must rely on an upstream result.

### Crews

Crews coordinate agents and tasks. Use sequential execution when task order is explicit. Use hierarchical execution when a manager should delegate and coordinate work, while validating the manager configuration for the installed CrewAI version.

### Flows

Flows provide explicit event-driven orchestration, state management, and conditional routing. Use them when a process needs branching, state transitions, or deterministic control around crew execution.

## Recommended Design Workflow

1. Define the final outcome and acceptance criteria.
2. Decide whether a single agent or deterministic function is sufficient.
3. Identify distinct responsibilities that justify multiple agents.
4. Define each agent's role, goal, and boundaries.
5. Break the work into tasks with clear inputs and outputs.
6. Map dependencies and context handoffs.
7. Choose sequential or hierarchical execution.
8. Use a Flow for explicit branching or state management.
9. Add tools with narrow permissions and validated inputs.
10. Configure iteration and rate limits appropriate to the workload.
11. Test agents and tools independently before testing the full crew.
12. Inspect intermediate outputs, final quality, token use, and failure behavior.

## Choosing Crews vs Flows

| Situation | Prefer |
|---|---|
| Small team completing ordered tasks | Sequential Crew |
| Manager delegates tasks to specialists | Hierarchical Crew |
| Conditional branching based on a result | Flow |
| Workflow state must be explicitly tracked | Flow |
| Events trigger different workflow steps | Flow |
| A crew is one stage in a larger process | Flow containing a Crew |
| Simple deterministic transformation | Regular code instead |

## References Already Included

| File | Focus |
|---|---|
| [Flows guide](references/flows.md) | Event-driven workflows, state management, branching, and crew integration |
| [Tools guide](references/tools.md) | Built-in tools, custom tools, MCP, and tool configuration |
| [Troubleshooting guide](references/troubleshooting.md) | Installation, agent, task, flow, tool, and performance issues |

## Included Resources

- [Crew design brief](resources/crew-design-brief.md): define roles, responsibilities, task boundaries, context, and success criteria.
- [Task handoff contract](resources/task-handoff-contract.md): make task inputs, outputs, dependencies, and failure behavior explicit.
- [Crew validation checklist](resources/crew-validation-checklist.md): test task flow, tools, limits, outputs, and operational safeguards.

## Security and Reliability

- Keep API keys in environment variables or an approved secret manager.
- Never commit credentials or paste them into prompts and logs.
- Restrict each tool to the smallest required permission set.
- Validate tool parameters before executing external actions.
- Avoid unsafe dynamic code execution such as evaluating untrusted expressions.
- Use bounded iterations, retries, timeouts, and rate limits.
- Require human approval for destructive or high-impact actions.
- Treat retrieved and tool-returned content as untrusted input.
- Review task outputs before passing them into consequential downstream actions.
- Measure the crew's output quality, latency, and token cost.

## Repository Structure

~~~text
claude-agents-crewai-skill/
├── SKILL.md
├── README.md
├── LICENSE
├── references/
│   ├── flows.md
│   ├── tools.md
│   └── troubleshooting.md
└── resources/
    ├── crew-design-brief.md
    ├── crew-validation-checklist.md
    └── task-handoff-contract.md
~~~

## External Resources

- [CrewAI documentation](https://docs.crewai.com)
- [CrewAI GitHub repository](https://github.com/crewAIInc/crewAI)
- [CrewAI tools](https://github.com/crewAIInc/crewAI-tools)
- [CrewAI examples](https://github.com/crewAIInc/crewAI-examples)

## License

Released under the MIT License. Copyright (c) 2026 Brajesh Kumar. See the root LICENSE file for the complete terms.
