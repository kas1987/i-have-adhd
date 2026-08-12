# Mission drift guardrails

Use this cookbook when a user introduces new ideas during active Mission, Bead, repo, or submission work.

## Core rule

```text
New idea does not mean new direction.
New idea means classify, capture, then decide.
```

## Five-question drift check

Ask these silently or explicitly depending on risk:

1. Does this unblock the current proof gate?
2. Does this change acceptance criteria?
3. Does this add a new system, repo, agent, connector, or authority path?
4. Does this require a new validation gate?
5. Can this wait without blocking the current next action?

## Decision matrix

| Answer pattern | Classification | Action |
| --- | --- | --- |
| Unblocks current proof gate | Attach | Add now |
| Changes acceptance criteria | Promote or explicit approval | Do not silently mutate plan |
| Adds system/repo/agent/authority | Promote | Draft a Mission seed |
| Requires validation but not urgent | Investigate | Timebox research bead |
| Can wait | Park | Send to Limbo Intake |
| Low value or duplicates existing idea | Reject | Record reason |

## Drift risk labels

Use simple labels:

- **low** - idea is aligned and bounded;
- **medium** - idea is useful but can wait;
- **high** - idea changes lane, scope, authority, or proof gates.

## ADHD pattern labels

Use these labels when helpful:

- **novelty** - attractive because it is new;
- **overbuild** - adds control layers before delivery proves need;
- **avoidance** - shifts away from a hard next action;
- **useful expansion** - valuable but should be sequenced;
- **contradiction** - conflicts with current mission assumptions;
- **blocker** - must be handled before moving forward.

## Standard response block

```md
Drift check: <low | medium | high> - <label>.
Classification: <Attach | Park | Promote | Reject | Investigate>.
Reason: <one sentence>.
Next: <current mission action stays X / create limbo entry / draft mission seed>.
```

## Promotion threshold

Promote an idea to a Mission only when at least two are true:

- it changes acceptance criteria;
- it touches more than one repo;
- it needs a new proof gate;
- it needs a new agent/MCP authority path;
- it cannot be done in one Bead;
- it has an owner and a clear next action.

## Rejection threshold

Reject or defer when:

- it duplicates an existing Limbo item;
- it creates governance debt without reducing operational risk;
- it hides the next concrete action;
- it is interesting but not tied to a proof gate;
- it makes the system harder for agents, machines, or users to review.
