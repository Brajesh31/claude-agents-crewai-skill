# CrewAI Agents Skill

A Claude skill for building and operating multi-agent systems with CrewAI. It focuses on role-based agent collaboration, task delegation, tool integration, and workflow design, with additional reference guides for flows, tools, and troubleshooting.

## What This Skill Covers

- Designing specialised agents with clear roles, goals, and backstories.
- Defining tasks and assigning responsibilities across a crew.
- Coordinating sequential and collaborative execution.
- Connecting tools that let agents interact with external systems.
- Structuring event-driven workflows with CrewAI Flows.
- Diagnosing common configuration and execution issues.

## Repository Structure

- `SKILL.md`: Main CrewAI skill instructions and core concepts.
- `references/flows.md`: Reference material for building structured CrewAI flows.
- `references/tools.md`: Guidance on tools and agent capabilities.
- `references/troubleshooting.md`: Common problems and troubleshooting guidance.
- `LICENSE`: MIT License for this repository.

## When to Use It

Use this skill when a project benefits from multiple specialised agents working together, when tasks need explicit delegation, or when a workflow needs to combine agent reasoning with tools and deterministic steps. It is also useful when deciding how to structure a CrewAI application before implementation.

## Getting Started

1. Review the main skill instructions and the CrewAI concepts they introduce.
2. Define the outcome the crew must achieve.
3. Create focused agent roles and give each one a clear responsibility.
4. Break the workflow into tasks with explicit expected outputs.
5. Add tools only where agents need external capabilities.
6. Use flows when the process requires structured control or event-driven orchestration.
7. Test the crew with representative inputs and consult the reference guides when issues arise.

## Design Guidance

Avoid creating agents simply to increase the number of participants. Extra roles add coordination overhead. Start with the smallest crew that can complete the workflow, then add specialisation only when it improves quality, clarity, or maintainability.

## License

Released under the MIT License. See [LICENSE](LICENSE) for details.
