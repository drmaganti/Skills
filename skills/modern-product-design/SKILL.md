---
name: modern-product-design
description: Design and implement polished, contemporary websites and product interfaces using a deliberate visual system, concrete references, strong typography, purposeful motion, responsive behavior, and visual QA. Use for landing pages, marketing sites, dashboards, SaaS products, app screens, and UI redesigns where visual quality matters.
---

# Modern Product Design

## Purpose

Create interfaces that feel intentionally art-directed rather than like generic AI-generated templates. Treat product strategy, design system, visual composition, implementation, and verification as separate but connected stages.

## Activate when

Use this skill when the user asks to:

- design or redesign a website, landing page, dashboard, SaaS interface, or application UI;
- create a high-fidelity product mockup or interactive prototype;
- modernize an existing interface;
- translate product requirements into a polished visual system;
- implement an approved visual direction in code;
- improve a site that looks generic, template-like, or visually inconsistent.

## Do not activate when

Do not take over tasks that are primarily:

- backend or infrastructure work with no meaningful visual surface;
- simple bug fixes that do not affect product design;
- isolated copywriting tasks;
- data analysis or research with no interface deliverable;
- requests where an existing locked design system must be followed without reinterpretation.

## Core principles

1. **Strategy before styling.** Understand the audience, product goal, primary action, information hierarchy, required content, and constraints before choosing visual treatment.
2. **Use references, not adjectives.** Prefer screenshots, real sites, component examples, sketches, or explicit design references over vague instructions such as “modern,” “premium,” or “clean.”
3. **Establish a system once.** Define typography, color, spacing, grids, radii, component behavior, imagery, iconography, and motion before expanding across many screens.
4. **Avoid generic AI composition.** Do not default to centered gradient hero + three equal cards + pill buttons + oversized rounded containers unless the product truly calls for them.
5. **Typography does most of the work.** Treat font selection, scale, width, line-height, contrast, and rhythm as primary design decisions.
6. **Whitespace must be intentional.** Use spacing to establish hierarchy, not merely to make the page feel sparse.
7. **Motion must communicate.** Animation should reveal hierarchy, continuity, state, depth, or progression. Avoid movement that exists only to look impressive.
8. **Design responsive behavior, not just desktop appearance.** Explicitly consider mobile hierarchy, wrapping, touch targets, navigation, dense data, and reduced-motion behavior.
9. **Iterate one visual dimension at a time.** When refining a design, isolate the problem: layout, typography, palette, density, imagery, component treatment, or motion.
10. **Verify visually.** A coded page is not complete until it is rendered and compared against the intended design.

## Workflow

### 1. Define the product frame

Capture:

- target user;
- job to be done;
- primary conversion/action;
- required sections/screens;
- content hierarchy;
- brand constraints;
- accessibility requirements;
- technical stack if implementation is requested.

For a simple single-page marketing site, move to high fidelity once the page structure is understood. For multi-screen applications or complex workflows, define the user flow and product requirements first.

### 2. Collect visual references

Use concrete references for:

- overall art direction;
- typography;
- navigation;
- hero composition;
- cards/data display;
- interaction/motion;
- backgrounds and visual texture;
- mobile behavior.

Use the resource catalog in `REFERENCES.md` for discovery. Do not copy a reference wholesale. Extract the useful design decisions and adapt them to the product.

### 3. Create the design system

Define the system using `DESIGN_SYSTEM_TEMPLATE.md` or an equivalent project file.

At minimum specify:

- type families and type scale;
- color tokens and semantic colors;
- spacing scale;
- content and grid widths;
- border/radius rules;
- elevation/shadow rules;
- button hierarchy;
- cards and surfaces;
- forms and inputs;
- navigation;
- icon treatment;
- image/art direction;
- motion principles;
- responsive breakpoints/behavior;
- accessibility and reduced-motion rules;
- explicit anti-patterns for the project.

### 4. Design the first high-value surface

Start with the screen or viewport that establishes the strongest visual language, usually the landing-page first viewport, application home/dashboard, or core task screen.

Do not produce every screen before validating the direction.

### 5. Refine deliberately

When feedback is needed, compare alternatives along one dimension at a time. Examples:

- denser vs more editorial layout;
- serif vs grotesk display typography;
- flat vs layered surfaces;
- restrained vs expressive motion;
- monochrome vs accent-led palette.

Preserve already-approved decisions unless the user asks to revisit them.

### 6. Implement with real components

For React/Tailwind projects, prefer production-ready source components that can be adapted locally. 21st.dev is a useful discovery source because its components follow React/Tailwind/shadcn conventions and can be handed to Codex as implementation prompts.

Do not add third-party visual dependencies merely because they look impressive. Consider bundle size, maintenance, accessibility, licensing, and consistency with the project system.

### 7. Visual QA

Render the implementation at representative widths and inspect:

- hierarchy;
- type wrapping;
- alignment;
- spacing rhythm;
- overflow;
- contrast;
- touch targets;
- hover/focus states;
- animation timing;
- mobile navigation;
- reduced-motion fallback;
- consistency with the approved design system.

Fix the largest perceptual mismatch first. Re-render after material changes.

## Modern-design anti-patterns

Avoid by default:

- purple/blue AI gradients used without brand rationale;
- excessive glassmorphism;
- every element inside a rounded card;
- excessive pill-shaped controls;
- identical three-column feature grids repeated down the page;
- huge headlines with weak supporting hierarchy;
- decorative floating blobs with no composition purpose;
- random gradients on text;
- excessive shadow stacks;
- animation on every element;
- stock imagery that does not reinforce the product story;
- desktop-first layouts that simply stack on mobile;
- low-contrast gray-on-gray interfaces;
- copying the visual style of a reference without adapting it to the product.

## Codex usage

For project-local automatic discovery, copy this folder to:

```text
.agents/skills/modern-product-design/
```

Then ask Codex to use the `modern-product-design` skill for the design or implementation task.

Recommended project context:

```text
PRD.md
USER_FLOWS.md
DESIGN_SYSTEM.md
REFERENCES.md
COMPONENTS.md
```

If ScrollCraft is appropriate for a highly cinematic or scroll-driven marketing experience, use its complete upstream skill separately rather than copying fragments into this skill. See `REFERENCES.md`.

## Quality gate

Before declaring the design complete, verify:

- [ ] The primary user and primary action are obvious.
- [ ] The interface has a coherent design system rather than per-screen styling.
- [ ] At least one concrete visual reference informed the direction when references were available.
- [ ] Typography hierarchy is deliberate and readable.
- [ ] The composition does not rely on generic AI-site patterns by default.
- [ ] Components are consistent and states are defined.
- [ ] Mobile behavior is intentionally designed.
- [ ] Accessibility and reduced motion are considered.
- [ ] Motion, if present, has a functional or storytelling purpose.
- [ ] The implementation has been visually rendered and checked when code is part of the task.
- [ ] External components/assets have been adapted to the project and their licensing/dependency implications considered.
