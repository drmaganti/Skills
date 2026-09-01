# Contributing

## When a new skill belongs here

Add a skill when the workflow is:

- repeated often enough that rediscovering instructions is wasteful;
- bounded enough to define when it should activate;
- important enough to benefit from explicit quality checks;
- reusable across more than one conversation/task.

Do not create a skill for a one-off prompt or a vague topic area with no repeatable workflow.

## Recommended skill structure

A skill should contain, as applicable:

1. metadata/name/description;
2. clear activation criteria;
3. important non-activation boundaries;
4. core rules;
5. execution workflow;
6. output/format guidance;
7. evidence/safety constraints;
8. a quality gate.

## Writing rules

- Use imperative, executable instructions.
- Prefer explicit decisions to inspirational prose.
- State what to do when information is missing.
- Never instruct the model to invent sources, metrics, identity facts, customer evidence, or technical behavior.
- Avoid provider-specific details unless the behavior genuinely depends on that provider.
- Keep examples short enough that they clarify rather than dominate the instruction set.

## Activation quality

The description/activation section should minimize both:

- **false positives** — the skill takes over requests it should not handle;
- **false negatives** — obvious matching tasks fail to use the skill.

Review activation wording against representative examples before merging.

## Change checklist

- [ ] Purpose/job is explicit.
- [ ] Activation boundary is clear.
- [ ] Missing-information behavior is defined.
- [ ] Evidence/factuality constraints are present where needed.
- [ ] Workflow is executable in order.
- [ ] Quality gate tests the important failure modes.
- [ ] Instructions do not conflict with higher-level safety/platform requirements.
- [ ] New complexity solves a repeated observed problem.

## Reviews

For material changes, review with at least a small fixture set of prompts:

- obvious positive cases;
- borderline activation cases;
- obvious non-matches;
- missing-context cases;
- one or more failure/adversarial cases relevant to the task.

Record meaningful behavioral changes in commit messages or a future changelog if the library grows.

## Repository organization

With one skill, keeping `SKILL.md` at the root is simplest. When multiple independent skills exist, migrate to a directory-per-skill structure and add an index rather than accumulating unrelated root files.
