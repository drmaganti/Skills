# Project Design System Template

Use this file once a visual direction is chosen. Replace placeholders with project decisions; do not leave multiple competing choices in the final system.

## 1. Brand intent

- Product:
- Audience:
- Brand attributes:
- Desired emotional impression:
- Primary action:
- Visual references:
- Explicitly avoid:

## 2. Typography

### Families

- Display:
- Body/UI:
- Mono/data (if needed):

### Scale

- Display XL:
- H1:
- H2:
- H3:
- Body L:
- Body:
- Small:
- Label:

For each define size, line-height, weight, tracking, and expected max line length where relevant.

### Rules

- Headline wrapping:
- Body max width:
- Numeric/data treatment:
- Uppercase usage:
- Emphasis rules:

## 3. Color

### Core tokens

- Background:
- Surface:
- Elevated surface:
- Primary text:
- Secondary text:
- Muted text:
- Border:
- Accent:
- Accent foreground:

### Semantic tokens

- Success:
- Warning:
- Danger:
- Info:
- Focus:

### Rules

- Dark/light mode:
- Gradient use:
- Contrast minimums:
- Data visualization palette:

## 4. Layout and grid

- Max content width:
- Wide content width:
- Page gutters desktop/tablet/mobile:
- Column grid:
- Section vertical rhythm:
- Text column width:
- Dashboard density rules:

## 5. Spacing

Define a small token scale and use it consistently.

Example structure:

```text
space-1
space-2
space-3
space-4
space-6
space-8
space-12
space-16
space-24
```

Document exceptions rather than creating arbitrary one-off values.

## 6. Shape and borders

- Small radius:
- Default radius:
- Large radius:
- Pill usage:
- Border width/style:
- Divider treatment:

State explicitly where rounded containers should *not* be used.

## 7. Elevation

- Base surface:
- Raised surface:
- Overlay:
- Modal/popover:

Prefer restrained elevation. Define shadows by role rather than by visual whim.

## 8. Buttons and actions

### Hierarchy

- Primary:
- Secondary:
- Tertiary/text:
- Destructive:

### States

- Default:
- Hover:
- Active:
- Focus:
- Disabled:
- Loading:

### Rules

- Minimum touch target:
- Icon placement:
- Button radius:
- When full-width is allowed:

## 9. Cards and surfaces

- Card purpose:
- Padding:
- Border/elevation:
- Heading treatment:
- Interactive states:
- Dense-data variant:

Avoid turning every content group into a card. Use whitespace, rules, typography, and grid alignment where a container is unnecessary.

## 10. Forms

- Input height:
- Label style:
- Placeholder style:
- Focus treatment:
- Validation messages:
- Error treatment:
- Help text:
- Select/menu behavior:

## 11. Navigation

- Desktop navigation:
- Mobile navigation:
- Active state:
- Sticky behavior:
- Scrolled state:
- Breadcrumbs/back behavior:

## 12. Iconography

- Icon set/source:
- Stroke/fill style:
- Default sizes:
- Decorative icon rules:
- Icon-only control requirements:

## 13. Imagery and visual art direction

- Photography/illustration style:
- Image aspect ratios:
- Cropping rules:
- Background treatment:
- Texture/noise usage:
- 3D/shader usage:
- Empty-state illustration rules:

## 14. Motion

### Principles

- What motion communicates:
- Standard duration:
- Emphasis duration:
- Easing:
- Enter/exit behavior:
- Scroll behavior:
- Hover behavior:

### Reduced motion

Define the fallback for users who prefer reduced motion. Do not make content comprehension depend on animation.

## 15. Responsive behavior

### Breakpoints

- Mobile:
- Tablet:
- Desktop:
- Wide:

### Rules

- Heading scaling:
- Grid collapse:
- Navigation change:
- Dense-table behavior:
- Card stacking:
- Media behavior:
- Sticky elements:
- Touch interactions:

## 16. Accessibility

- Contrast standard:
- Focus visibility:
- Keyboard navigation:
- Screen-reader labels:
- Motion preferences:
- Touch target minimum:
- Error identification:

## 17. Product-specific components

List the distinctive reusable product components and their variants, for example:

- KPI tile
- opportunity card
- stock recommendation panel
- comparison table
- onboarding stepper
- recommendation explanation
- confidence indicator

For each define anatomy, variants, states, and responsive behavior.

## 18. Anti-patterns for this project

Document visual patterns that should not appear unless explicitly approved.

Examples:

- no generic purple AI gradients;
- no excessive glassmorphism;
- no repeated three-card feature rows;
- no pill treatment for every control;
- no decorative motion without purpose;
- no low-contrast gray body text;
- no unapproved fonts or arbitrary color values;
- no new radius/shadow styles outside tokens.

## 19. Reference mapping

For every key reference, record exactly what is being borrowed conceptually.

| Reference | Use | Do not copy |
| --- | --- | --- |
| Example site/screenshot | Editorial typography and hero proportions | Brand, copy, imagery, exact layout |

## 20. Approval status

- Art direction approved:
- Typography approved:
- Palette approved:
- Core components approved:
- Motion direction approved:
- Mobile direction approved:
- Last updated:
