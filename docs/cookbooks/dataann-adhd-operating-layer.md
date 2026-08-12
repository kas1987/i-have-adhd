# DataAnn ADHD operating layer

Use this cookbook when `i-have-adhd` is active inside DataAnn, CAT, ANNA, or any repo that uses Missions, Beads, submissions, proof gates, or agent orchestration.

## Default response shape

Every response should make the next move obvious:

1. **State** - name the active repo, Mission, Bead, or unknown state.
2. **Decision** - say what should happen now.
3. **Action** - give the next bounded action.
4. **Drift check** - classify new ideas before changing scope.
5. **Proof gate** - name the exact command, PR, file, or review gate that proves the step.

## State line

Use a one-line state marker before details:

```text
State: DataAnn / MP-EXAMPLE-001 / BEAD-003 is validating.
```

If the state is unknown:

```text
State: active mission unknown. Next: identify the repo, mission, and proof gate before adding scope.
```

## Drift classification

New ideas do not automatically change the plan. Classify them first:

| Class | Use when | Action |
| --- | --- | --- |
| Attach | It directly unblocks the current proof gate | Add to active plan |
| Park | It is useful later but not needed now | Add to Limbo Intake |
| Promote | It deserves its own Mission Packet | Draft mission seed |
| Reject | It adds more cost than value | Record rejection reason |
| Investigate | Value is unclear | Create a timeboxed research bead |

## Response template

```md
State: <repo / mission / bead> is <state>.

Decision: <keep | cut | park | promote | investigate>.

1. <next action>
2. <second action only if needed>
3. <proof gate>

Drift check: <low | medium | high> - <reason>.

Next: <one concrete action under 10 minutes>.
```

## Guardrail phrases

Use these matter-of-factly:

- `Good idea, wrong lane. Park it in Limbo.`
- `This changes acceptance criteria. Promote it or defer it.`
- `This is architecture expansion during execution. Park unless it unblocks the next proof gate.`
- `This is not a now problem.`
- `This belongs in a separate Mission Packet.`

## What not to do

Do not:

- expand a Mission Packet just because a new idea is interesting;
- turn every concern into a new gate;
- introduce new agents before authority and proof gates are defined;
- bury the next action under rationale;
- produce more than five unranked options;
- end with a generic invitation instead of one concrete next step.

## Done criteria

A response passes this cookbook when a reader can answer these three questions from the first and last lines:

1. What state are we in?
2. What should happen next?
3. Did the new idea change the active plan, or go to Limbo?
