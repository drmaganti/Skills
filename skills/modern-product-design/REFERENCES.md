# Modern Product Design — Reference Catalog

These resources are inputs to the design workflow, not substitutes for product thinking or a coherent design system.

## Component and interface sources

### 21st.dev

- URL: https://21st.dev/
- Use for: modern React/Tailwind/shadcn-compatible components, animated heroes, navigation, cards, shaders, gradients, and interaction patterns.
- Best practice: choose a specific component or pattern, then adapt typography, spacing, color, motion, and states to the project design system rather than dropping it in unchanged.
- Codex note: 21st.dev exposes AI-ready component prompts that can be handed directly to coding agents.

## Visual inspiration

### Godly

- URL: https://godly.design/
- Use for: contemporary website art direction, layout, typography, composition, and interaction references.
- Best practice: identify what specifically works in a reference—e.g. hero proportions, editorial type treatment, section rhythm, navigation behavior—rather than asking to “make it look like” an entire site.

### Awwwards

- URL: https://www.awwwards.com/
- Use for: high-end web art direction, experimental composition, motion, typography, and interaction patterns.
- Best practice: use selectively. Award-oriented patterns can prioritize spectacle over usability, accessibility, performance, or conversion. Borrow the idea, not necessarily the implementation complexity.

### MotionSites

- URL: https://motionsites.org/
- Use for: website motion ideas, animated backgrounds, sections, product-site directions, hero treatments, and motion-oriented prompts.
- Best practice: treat motion as part of hierarchy and storytelling. Always define reduced-motion behavior and confirm that animation does not harm usability or performance.

## Reusable agent skills

### ScrollCraft — Nate Herk

- Repository: https://github.com/nateherkai/scroll-craft
- Use for: premium, scroll-driven marketing websites where scroll itself is part of the storytelling timeline.
- Codex support: the upstream project documents installing the complete `scroll-craft` skill folder into a project’s `.agents/skills/` directory.
- Important: keep the upstream folder intact. Do not copy isolated portions of the skill because its references, scripts, templates, and verification workflow are designed to work together.
- Use selectively: it is best suited to cinematic marketing experiences, not every SaaS dashboard or transactional product interface.

### HyperFrames

- Repository: https://github.com/heygen-com/hyperframes
- Skill file: https://github.com/heygen-com/hyperframes/blob/main/skills/hyperframes/SKILL.md
- Use for: motion graphics, animation, rendered visual compositions, promo/explainer work, title cards, overlays, and related video/motion workflows.
- Use selectively: this is primarily a motion/video capability rather than a general application UI design system.

## Implementation foundation

### shadcn/ui

- URL: https://ui.shadcn.com/
- Use for: accessible, editable React component foundations that can be styled into a project-specific system.
- Best practice: treat shadcn/ui as infrastructure, not as the final visual identity. Customize tokens, typography, density, radii, states, and composition.

## Recommended combinations

### Product dashboard / SaaS application

1. Product requirements and flows
2. Project design system
3. Godly for art direction references
4. 21st.dev for selected component ideas
5. shadcn/ui as implementation foundation where appropriate
6. Rendered visual QA

### Modern marketing site

1. Positioning and page narrative
2. Godly + Awwwards for art direction
3. 21st.dev for production-ready interaction/component ideas
4. MotionSites for motion references
5. Project design system
6. Visual QA at desktop and mobile widths

### Cinematic scroll-driven launch page

1. Positioning and narrative
2. Concrete visual references
3. Project design system
4. ScrollCraft as the specialized execution skill
5. Performance, accessibility, reduced-motion, and visual verification pass

## Reference-use rules

- Do not copy a complete commercial site or protected visual identity.
- Extract principles and patterns, then reinterpret them for the current brand and product.
- Verify current licensing before shipping third-party code, assets, fonts, video, imagery, or templates.
- Prefer the smallest external dependency that achieves the required effect.
- Do not introduce visual complexity without a product or storytelling reason.
