# CrewAI Task Handoff Contract

Use this contract whenever one task depends on another task's output. Clear handoffs reduce hidden assumptions and prevent downstream agents from treating incomplete work as final.

## Handoff Metadata

- **Upstream task:**
- **Upstream agent:**
- **Downstream task:**
- **Downstream agent:**
- **Dependency type:** required / optional / review-only

## Input Contract

- **Required input fields:**
- **Data types and formats:**
- **Units, time zone, or naming conventions:**
- **Source references or provenance:**
- **Allowed assumptions:**
- **Forbidden assumptions:**

## Output Contract

- **Required deliverable:**
- **Expected structure:**
- **Evidence or citations required:**
- **Validation rules:**
- **Known uncertainty to preserve:**
- **Definition of complete:**

## Failure Behavior

- **Missing input behavior:**
- **Invalid output behavior:**
- **Upstream task failure behavior:**
- **Retry policy:**
- **Escalation / clarification owner:**

## Handoff Review

- [ ] Output conforms to the agreed structure.
- [ ] Required evidence and source references are present.
- [ ] Uncertainty and limitations are retained.
- [ ] No unsupported facts are introduced during handoff.
- [ ] Downstream agent has the context required to proceed.
- [ ] Incomplete or failed output is not silently treated as success.

## Handoff Record

- **Status:** accepted / accepted with caveats / rejected
- **Reviewer:**
- **Reason:**
- **Follow-up action:**
