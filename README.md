# Skills

A library of reusable **AI task skills**: structured instruction files that define when a capability should activate, how work should be performed, and what quality checks must pass before output is delivered.

## Skills

### Article Writing

[`skills/article-writing/SKILL.md`](./skills/article-writing/SKILL.md)

For evidence-based long-form content that matches supplied voice/brand guidance while avoiding generic AI-writing patterns.

Covers:

- articles, guides, blog posts, tutorials, and newsletters;
- voice capture from supplied examples;
- evidence-first structure;
- rules against invented metrics/biographical claims;
- banned generic/hype patterns;
- technical-guide, essay, and newsletter structure;
- final factuality, structure, voice, and formatting checks.

### Modern Product Design

[`skills/modern-product-design/SKILL.md`](./skills/modern-product-design/SKILL.md)

For polished modern websites, landing pages, dashboards, SaaS interfaces, application screens, redesigns, and high-fidelity prototypes.

Covers:

- strategy before styling;
- concrete visual references instead of vague style adjectives;
- reusable product design systems;
- modern typography, layout, spacing, surfaces, and motion;
- avoidance of common AI-generated website patterns;
- responsive behavior and accessibility;
- Codex-compatible usage via `.agents/skills/`;
- implementation and rendered visual QA.

Companion files:

- [`REFERENCES.md`](./skills/modern-product-design/REFERENCES.md) — 21st.dev, Godly, Awwwards, MotionSites, ScrollCraft, HyperFrames, shadcn/ui, and recommended combinations.
- [`DESIGN_SYSTEM_TEMPLATE.md`](./skills/modern-product-design/DESIGN_SYSTEM_TEMPLATE.md) — reusable template for typography, colors, spacing, grids, components, motion, responsive behavior, accessibility, anti-patterns, and approvals.

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

## Repository structure

```text
README.md
CONTRIBUTING.md
MAINTENANCE.md
skills/
  article-writing/
    SKILL.md
  modern-product-design/
    SKILL.md
    REFERENCES.md
    DESIGN_SYSTEM_TEMPLATE.md
```

## Using a skill

Provide the relevant `SKILL.md` to an AI system that supports reusable instructions/skills, or use it as the source-of-truth instruction set when performing that task.

For Codex project-local discovery, a skill can be copied into:

```text
.agents/skills/<skill-name>/
```

Keep companion files with the skill when the workflow references them.

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

Active reference/library repository. Add a new skill when a repeated workflow benefits from a durable, testable instruction contract.
