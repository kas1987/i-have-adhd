# Skill Contracts

`SKILL.md` should stay short enough to remain usable as an always-on control plane.

## LOC contract

| LOC in `SKILL.md` | Status | Required action |
|---:|---|---|
| 1-200 | Pass | Normal review. |
| 201-299 | Warning | Human review and timestamped HITL acceptance required. |
| 300+ | Fail | Refactor before merge. No acceptance override. |

## HITL acceptance

If a skill exceeds 200 LOC during creation or edit, add:

```text
docs/skill-hitl-acceptance/<skill-name>.md
```

Required fields:

```yaml
skill: <skill-name>
accepted_by: <human reviewer>
accepted_at: YYYY-MM-DDTHH:MM:SS-04:00
decision: accepted
reason: <why this skill is allowed to exceed 200 LOC>
review_scope: <what was reviewed>
follow_up: <refactor plan or N/A>
```

## Refactor at 300 LOC

At 300 LOC or above, the skill must be split. Move optional detail into cookbooks, examples, schemas, scripts, or separate skills.

## Command

```bash
npm run check-skill-contracts
```
