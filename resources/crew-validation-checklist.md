# CrewAI Validation Checklist

Use this checklist before accepting a crew or promoting it to a higher-impact environment.

## Architecture and Roles

- [ ] Multiple agents are justified by distinct responsibilities.
- [ ] Each role has clear boundaries.
- [ ] Tasks are assigned to the right agents.
- [ ] The chosen process matches the dependency structure.
- [ ] A Flow is used when explicit state or branching is needed.

## Task Design

- [ ] Task descriptions specify the required work.
- [ ] Expected outputs are observable and specific.
- [ ] Context dependencies are explicitly connected.
- [ ] Output schemas are used where structured data is required.
- [ ] Downstream tasks handle incomplete or invalid inputs.

## Tools and Permissions

- [ ] Each tool has a clear, narrow responsibility.
- [ ] Tool inputs are validated.
- [ ] External API calls have timeouts and error handling.
- [ ] Credentials are not embedded in code or prompts.
- [ ] Unsafe dynamic execution is avoided.
- [ ] Destructive actions require approval.

## Execution Controls

- [ ] Iteration limits are configured.
- [ ] Rate limits match provider constraints.
- [ ] Retry behavior is bounded.
- [ ] Memory is enabled only when required.
- [ ] Logs and task outputs are observable.
- [ ] Failure branches and escalation are defined.

## Quality and Cost

- [ ] Agents are tested individually.
- [ ] The complete crew is tested on representative cases.
- [ ] Final outputs are checked against acceptance criteria.
- [ ] Token usage and execution time are recorded.
- [ ] Results are compared with a simpler baseline.
- [ ] Known failure modes are documented.

## Release Decision

- **Crew / project version:**
- **Reviewer:**
- **Known limitations:**
- **Decision:** approve / conditional / reject
- **Date:**
