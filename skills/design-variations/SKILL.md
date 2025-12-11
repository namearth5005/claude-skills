---
name: design-variations
description: Create systematic variations of reference designs while maintaining quality. Use when the user provides a reference image, existing code, or design to create variations from. Analyzes what makes the reference work, then produces distinctive alternatives along specified dimensions. Works with screenshots, Figma references, or existing HTML/CSS/React code. Pairs with frontend-design skill for quality standards.
---

# Design Variations

Create thoughtful variations from reference designs. Each variation should be a fully-realized design that could stand alone — not a mechanical filter swap.

**Core principle**: Leverage frontend-design's quality bar. Every variation must be as intentionally designed as if created from scratch.

## Workflow

1. **Analyze** — Deconstruct the reference
2. **Identify** — What's core identity vs. variable
3. **Propose** — Variation directions with rationale
4. **Execute** — Build each as a complete design

## Step 1: Analyze the Reference

Extract these elements:

### Visual DNA
- **Color system**: Primary, secondary, accent, neutrals. Ratios and relationships.
- **Typography**: Font families, scale, weights, hierarchy
- **Spacing system**: Base unit, rhythm, density
- **Layout structure**: Grid, alignment, visual flow
- **Visual effects**: Shadows, borders, gradients, textures
- **Motion patterns**: Transitions, animations, timing

### What Makes It Work
Ask: Why is this design effective?
- Is it the contrast?
- The restraint?
- The unexpected color?
- The typography pairing?
- The spatial rhythm?

Name the 2-3 things that make it *this* design.

## Step 2: Identify Core vs. Variable

| Preserve (Core Identity) | Can Vary |
|--------------------------|----------|
| Overall layout structure | Color palette |
| Content hierarchy | Typography choices |
| Functional patterns | Spacing density |
| Brand-critical elements | Visual effects |
| User flow | Mood/tone |

**User can override**: If they say "keep the colors, vary the layout" — follow their lead.

## Step 3: Propose Variation Directions

Before building, propose 3-5 variation directions with rationale:

**Example proposals:**

> **Variation A: Warmer & Organic**
> Shift palette toward terracotta/sage. Soften corners. Add subtle texture. Keeps the minimal layout but feels more approachable.

> **Variation B: High Contrast Editorial**
> Push to near-black and white with one sharp accent. Tighten typography. Add dramatic negative space. Same structure, more intensity.

> **Variation C: Playful & Saturated**  
> Vibrant complementary colors. Rounder elements. Slightly looser spacing. Maintains hierarchy but feels energetic.

Let user select or refine before executing.

## Step 4: Execute with Frontend-Design Quality

Each variation must meet frontend-design standards:

### Typography
- Distinctive font choices (never default to Inter, Roboto, Arial)
- Thoughtful pairing if using two families
- Proper hierarchy and scale

### Color
- Committed palette, not timid
- Intentional contrast ratios
- Cohesive across all elements

### Details
- Consistent spacing system
- Purposeful visual effects (not decorative noise)
- Refined micro-interactions where appropriate

### Distinctiveness
- Each variation should feel like a *design decision*, not a theme toggle
- Avoid mechanical swaps (don't just run values through a formula)
- Each should be memorable in its own way

## Variation Dimensions

When user doesn't specify, vary across these:

### Mood Spectrum
`Clinical → Warm → Playful → Bold → Luxurious → Raw`

### Density Spectrum  
`Airy/Spacious → Balanced → Dense/Information-rich`

### Contrast Spectrum
`Subtle/Low-contrast → Balanced → High-contrast/Dramatic`

### Color Temperature
`Cool/Blue-shifted → Neutral → Warm/Earth tones`

## Output Format

For each variation, provide:

```
## Variation [A/B/C]: [Name]

**Direction**: [One-sentence description of the aesthetic shift]

**Key changes**:
- Color: [What changed and why]
- Typography: [What changed and why]  
- Spacing/Layout: [What changed and why]
- Details: [Any other notable shifts]

**Why it works**: [Brief rationale for this as a cohesive design]

[Full code implementation]
```

## Working with Different Inputs

### Reference Image (Screenshot/Photo)
1. Describe what you see in detail
2. Extract approximate values (colors, spacing ratios, font styles)
3. Note what you can't determine precisely
4. Build variations from your analysis

### Existing Code
1. Read and understand the full implementation
2. Extract design tokens (CSS variables, Tailwind classes, etc.)
3. Identify component patterns
4. Variations can be precise — you have exact values

### Verbal Description
1. Ask clarifying questions about the reference
2. Build a mental model before proposing variations
3. Confirm understanding before executing

## Anti-Patterns

- **Lazy swaps**: Just changing `--primary: blue` to `--primary: red`
- **Losing the soul**: Varying so much the reference is unrecognizable
- **Generic output**: Variations that look like default templates
- **Unfinished variations**: Treating any variation as "lesser" — each must be complete
- **Ignoring what works**: Varying the thing that made the original effective

## Example

**User provides**: Minimalist portfolio site, lots of white space, black text, single red accent, geometric sans-serif font

**Analysis**: Effectiveness comes from restraint and the tension of one bold accent against monochrome. Core = the contrast strategy. Variable = which accent, typography choice, spacing density.

**Proposed variations**:
- A: Keep monochrome strategy, swap red for deep terracotta, use refined serif
- B: Invert to dark mode, accent becomes light/warm, same geometric type
- C: Introduce subtle warm gray instead of pure white, forest green accent, slightly softer type

Each is a complete design. Each maintains the "restrained + one bold element" identity. Each is distinctive.
