# Maintenance

Reusable instructions become harmful when they stay authoritative after the workflow, platform, or evidence has changed. Skills therefore need a lightweight maintenance discipline.

## Review triggers

Review a skill when:

- repeated outputs fail in the same way;
- users routinely override part of the workflow;
- a platform/tool capability materially changes;
- an instruction conflicts with newer safety/product rules;
- examples or references become stale;
- activation is too broad or too narrow.

## Periodic review

For actively used skills, review at least quarterly for:

- activation precision;
- obsolete provider/platform assumptions;
- repeated failure modes;
- unnecessary verbosity;
- factual/evidence safeguards;
- whether the quality gate still checks the important risks.

## Change types

### Clarification

Improves wording without intentionally changing behavior.

### Behavioral change

Changes when the skill activates, how it executes, or what it returns. Test against representative prompts before merging.

### Breaking change

Changes the skill contract enough that existing consumers may behave differently. Document the change clearly and consider versioning if external consumers depend on it.

## Evidence discipline

If a skill refers to external standards, product behavior, APIs, laws, or other changing facts, either:

- keep the instruction generic and require current verification at execution time; or
- record the source/date and schedule review.

Do not freeze time-sensitive facts into durable instructions without a freshness strategy.

## Deprecation

Deprecate a skill when:

- the platform provides a better native capability;
- the workflow is no longer used;
- another skill fully subsumes it;
- maintenance cost exceeds its repeated value.

Keep a short explanation of the replacement or reason rather than leaving an obsolete skill that still looks active.

## Quality principle

The goal is not the largest skill library. The goal is a small collection of instruction contracts that reliably improve repeated work.
