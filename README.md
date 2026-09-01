# Skills

A small library of reusable **AI task skills**: structured instruction files that define when a capability should activate, how work should be performed, and what quality checks must pass before output is delivered.

The repository currently contains one skill:

- [`SKILL.md`](./SKILL.md) — **article-writing**, for producing evidence-based long-form content while matching supplied voice/brand guidance and avoiding generic AI-writing patterns.

## What a skill is

A skill is not a prompt snippet. It is a compact operating contract for a repeatable task.

A good skill should define:

- what job it performs;
- when it should and should not activate;
- inputs/context it needs;
- non-negotiable behavioral rules;
- a clear workflow;
- output/quality expectations;
- evidence or safety constraints where relevant.

The goal is to make high-quality behavior reusable without relying on a long conversation to rediscover the same instructions.

## Current article-writing skill

The current skill covers:

- long-form articles, guides, blog posts, tutorials, and newsletters;
- voice capture from supplied examples;
- evidence-first structure;
- rules against invented metrics/biographical claims;
- banned generic/hype patterns;
- different structural guidance for technical guides, essays, and newsletters;
- a final quality gate for factuality, structure, voice, and formatting.

## Repository structure

```text
README.md        repository purpose and usage
SKILL.md         current article-writing skill
CONTRIBUTING.md  standard for adding/changing skills
MAINTENANCE.md   review/version/freshness discipline
```

If the library grows, move each skill into a named directory while preserving a clear index, for example:

```text
skills/
  article-writing/
    SKILL.md
  market-research/
    SKILL.md
```

Do not reorganize solely for aesthetics while there is only one skill.

## Using a skill

Provide the relevant `SKILL.md` to an AI system that supports reusable instructions/skills, or use it as the source-of-truth instruction set when performing that task.

The consuming platform may have its own metadata/schema requirements; keep platform-specific packaging separate from the core behavioral content where practical.

## Design principles

- **Specific activation boundary.** A skill should not trigger on every vaguely related request.
- **Evidence before confidence.** Never instruct a model to invent facts to fill gaps.
- **Workflow over prose.** A user/agent should be able to execute the instructions consistently.
- **Quality gate included.** Define how the result is checked, not just how it is drafted.
- **Minimal standing context.** Keep skills concise enough to load when needed.
- **Platform independence where practical.** Prefer task logic that survives model/provider changes.

## Documentation

- [`CONTRIBUTING.md`](./CONTRIBUTING.md) — skill schema, contribution/review checklist
- [`MAINTENANCE.md`](./MAINTENANCE.md) — freshness, versioning, evidence, deprecation

## Status

Active reference/library repository. The current scope is intentionally small; add a new skill only when a repeated workflow benefits from a durable, testable instruction contract.
