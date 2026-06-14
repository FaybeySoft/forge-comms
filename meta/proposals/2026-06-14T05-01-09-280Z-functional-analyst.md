# Proposal — evolve `functional-analyst`

**Filed by:** manager (Captain Holt)
**When:** 2026-06-14T05:01:09.280Z

## Rationale

Forgebot-created issues and artifacts often lack acceptance criteria and are filed directly into missions, increasing clarification work and causing stalled missions (evidence: modelos-casas-canarias #276 artifacts and mission m-202605112016-trvk with issueCount=123).

## Proposed change

Add a mandate in the functional-analyst prompt: For any forgebot-created issue assigned to you, produce within 48 hours a one-paragraph scoping brief containing: 1) Goal statement, 2) Acceptance criteria (3 bullet points), 3) Test cases or validation steps, 4) Blockers/Dependencies. If the artifact is duplicate or out-of-scope, document the reason and recommend closure. When converting an artifact to a mission ticket, add a link to the brief and set the ticket's "definition of ready" to require the brief before development work starts.

## Next step

Human reviews this proposal and, if accepted, applies it via PR to `forge-agents`.