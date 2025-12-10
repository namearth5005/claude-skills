---
name: prompt-improver
description: Automatically enhances vague or suboptimal user prompts before execution. Activates when user requests are ambiguous, lack specificity, missing context, or could benefit from prompt engineering improvements. Use when the user's intent is clear but their prompt structure is weak. Do NOT use for already well-structured prompts or simple factual questions.
---

# Prompt Improver

Enhance weak prompts, then execute based on the improved version.

## Workflow

1. **Detect** — Identify prompt weaknesses (see Diagnosis Checklist)
2. **Improve** — Rewrite using applicable techniques
3. **Show** — Display the improved prompt in a callout block
4. **Execute** — Respond as if the improved prompt was the original request

## Diagnosis Checklist

Scan for these weaknesses:

| Weakness | Signal | Fix |
|----------|--------|-----|
| Vague | No specific outcome stated | Add explicit deliverable |
| No context | Missing purpose/audience/use-case | Add motivation |
| No constraints | Missing format/length/scope | Add boundaries |
| Ambiguous | Multiple interpretations possible | Clarify intent |
| Over-broad | Too many things requested at once | Focus or chunk |
| Missing examples | Complex format without demonstration | Add one-shot example |

If none of these apply, skip improvement and execute directly.

## Improvement Techniques

Apply selectively based on diagnosis:

**Clarity**: Lead with action verb, state exact deliverable
**Context**: Add why it matters, who it's for, how it'll be used
**Specificity**: Add constraints (format, length, audience, tone)
**Structure**: Break compound requests into clear steps
**Examples**: Add brief example of desired output format if complex

## Anti-Patterns to Avoid

- Over-engineering simple requests
- Adding unnecessary constraints the user didn't imply
- Changing the user's actual intent
- Making prompts longer without making them better
- Adding formality when casual was appropriate

## Output Format

```
> **Improved prompt:** [rewritten prompt here]

[Then immediately provide the response to the improved prompt]
```

## Examples

**User writes:** "Write about dogs"

**Improved prompt:** "Write a 300-word informative article about dogs as pets, covering their benefits for families, basic care needs, and popular breeds for first-time owners."

[Then Claude writes the article]

---

**User writes:** "Help with my code"

**Improved prompt:** "Review the code I'm about to share, identify bugs or inefficiencies, and suggest improvements with explanations."

[Then Claude asks for the code or proceeds if already provided]

---

**User writes:** "Make a presentation"

**Improved prompt:** "Create a 5-slide presentation structure. Please ask me about the topic, audience, and purpose so you can tailor the content appropriately."

[Then Claude asks clarifying questions]

## When to Skip

Execute directly without improvement when:
- Request is already specific and well-structured
- Simple factual question ("What's the capital of France?")
- User explicitly says "just answer" or "quick question"
- Conversational/social exchange ("How are you?")
