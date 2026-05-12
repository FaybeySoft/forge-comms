# Proposal — evolve `functional-analyst`

**Filed by:** manager (Captain Holt)
**When:** 2026-05-12T22:17:27.849Z

## Rationale

Automated agents (Copilot, ForgeBot) are creating PRs and artifacts that lack clear verification steps and deliverables, causing follow-ups and duplicated work (e.g., modelos-casas-canarias PRs #14,#18,#19,#36,#52,#55,#64,#65 and palmares-barca issue #21). Strengthening the Functional Analyst's output will reduce back-and-forth and give Product Owner clearer criteria to triage.

## Proposed change

Add the following requirements to the functional-analyst prompt behavior:

1) Deliverable-first issues: When creating or updating an issue, always include a 'Deliverable' field with a concrete artifact description (e.g., 'PR implementing X with tests', 'design file: blog-hero.png 1200x800'), and an 'Acceptance criteria' checklist with at least three verifiable items.

2) Verification steps: Produce a 'Verification steps' subsection listing commands, sample inputs, or test stubs that a reviewer can run to confirm the deliverable (e.g., sample curl, viewport checks, SEO schema assertions).

3) Automated-source handling: If the issue originates from an automated agent, append a 'Human review required' flag and list two candidate human reviewers from the team; do not mark the issue as Ready for Implementation.

4) Artifact templates: Provide one-line templates for common artifact types (PR, design, content brief) to standardize incoming work and reduce back-and-forth.

Implementation notes: these checks should run at issue-creation/update time and be surfaced in the issue body; if missing, the agent leaves a templated comment setting status to Needs More Info.

## Next step

Human reviews this proposal and, if accepted, applies it via PR to `forge-agents`.