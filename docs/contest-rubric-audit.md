# CALL-E contest rubric audit

Checked against the official rules and overview on 2026-08-09.

## Stage-one viability

| Requirement | Evidence | Status |
| --- | --- | --- |
| Functional software application | Node/TypeScript application and complete browser workflow | Implemented |
| CALL-E actually used at runtime | `CalleCallProvider` imports `CalleClient` and calls `client.calls.createAndWait` | Implemented; live success evidence pending |
| Consistent installation and operation | Node 24.14.0 and pnpm 11.16.0 pins, frozen lockfile, mock path, build, and 18 no-call tests | Freshly verified August 10 |
| New during contest period | Repository history and build package date are within the submission period | Must remain truthful at submission |
| Public contribution PR | `https://github.com/CALLE-AI/awesome-phone-call-agents/pull/133` | Open; August 10 safety feedback is addressed by explicit recipient binding, SDK idempotency, durable checkpoints, and fail-closed result validation; organizer re-review/merge pending |
| Public video under three minutes | Must show real app and real authorized CALL-E run | Pending live run and video |
| Free judge access | Mock workflow runs without credentials; source is public | Implemented locally; public deployment pending/optional |
| CALL-E account email | Private submission field | Bradley action |

## Equal judging criteria

### Real-world impact

Strengths:

- Resolves a concrete gap between a public safety notice and action by the owner.
- Useful for children's products, appliances, batteries, furniture, and tools.
- Does not depend on a retailer inventory API or a vendor partnership.

Evidence still needed:

- One real authorized call demonstrating that the structured result captures a meaningful qualification or remedy answer.

### Quality of the idea

Strengths:

- Phone is used for the unavailable last-mile answer, not as a novelty interface.
- Official public data anchors both the destination and the script.
- Minimum-data design and human handoff make the contribution reusable.

### Technical implementation

Strengths:

- Actual CALL-E SDK import and runtime call.
- Strict result schema plus terminal status, task completion, one-recipient binding, enum, confidence, and evidence validation before display.
- Provider abstraction with deterministic no-call test route.
- Authoritative server-side refetch before preview.
- Masking, TTL, single-use approval, stable SDK idempotency, a hash-only durable ambiguous-call checkpoint, body limit, CSP, and fail-closed validation.

Evidence still needed:

- Successful live CALL-E response on the authorized demo route.
- Organizer re-review/merge of the open validator-complete PR, plus any further requested changes.

### Product experience and demo

Strengths:

- Coherent four-step flow.
- Call side effect and runtime mode are visible.
- Result emphasizes an actionable plan instead of exposing a transcript.
- Responsive design with no third-party visual assets.

Evidence still needed:

- Visual browser review at desktop/mobile widths.
- Public sub-three-minute video with real runtime footage.

## Honest readiness

The public source repository and organizer PR now exist and are independently visible. The software is not submission-complete until the authorized live CALL-E run, public video, and final Devpost fields exist. Organizer review/merge of PR #133 remains pending. No win probability should be represented as certain; judging and field growth are outside the entrant's control.
