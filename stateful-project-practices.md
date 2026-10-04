# Stateful Project Practices

When a project spans multiple sessions, people, or tools, its history needs to travel with it. These practices help preserve working results and prevent repeated mistakes.

## 1. Establish the Baseline

Before changing anything, identify:

- The current authoritative version and where it lives.
- What works and has already been approved.
- Constraints and decisions that must be preserved.
- Known problems and unfinished work.

If sources disagree, resolve which is authoritative before proceeding.

## 2. Define the Change

State the intended outcome and how success will be checked.

Keep changes focused. A request to fix one feature does not authorize redesigning unrelated parts of the project.

## 3. Preserve a Way Back

Before making changes, retain an appropriate recovery point: a Git commit, backup, export, or previous version.

Record how to restore it. Git history preserves committed files; it does not automatically protect external systems, databases, or unpublished local work.

## 4. Make and Verify the Change

Use the smallest practical change that achieves the goal.

Check both:

- **The intended result:** Did the change solve the problem?
- **Preserved behavior:** Do the relevant existing features still work?

Match verification to the risk. A wording correction needs a review; a functional change may need tests and a working demonstration.

## 5. Record Decisions and Results

Document important decisions with a date and reason. When a decision changes, mark the earlier decision as superseded rather than silently erasing it.

Distinguish:

- Verified facts.
- Assumptions and estimates.
- Proposed actions.
- Completed and checked work.

## 6. Leave a Clear Handoff

At the end of a work session, update the project state:

- Current version or commit.
- What changed and what was verified.
- Unresolved questions or blockers.
- The next concrete action.
- Any required approval before publication or deployment.

Do not rely on chat history or someone's memory as the only project record.

## A Minimal Project Record

| Record | Purpose |
|---|---|
| `README.md` | Purpose, setup, usage, and entry points |
| `PROJECT_STATE.md` | Current baseline, constraints, status, and next action |
| `DECISIONS.md` | Important decisions and their reasons |
| Git history or change log | What changed and available recovery points |

Small projects can combine these records. Add structure only when it helps someone continue the work reliably.

## Reusable Instruction

> Before changing this project, identify its authoritative baseline and read its current state and decisions. Define the requested change, preserve unrelated approved behavior, retain a recovery point, and verify the result. Update the project record with what changed, what was checked, what remains unresolved, and the next action. If an unknown materially affects correctness or authorization, resolve it before proceeding.

## Contribute Your Experience

In Discussions, share a situation where project continuity broke down—or where a practice helped prevent it. Explain what happened, what you changed, and whether it worked.
