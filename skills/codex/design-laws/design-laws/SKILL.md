---
name: design-laws
description: Apply Laws of UX and adjacent design psychology when the user asks to design, review, critique, prioritize, or explain interfaces using psychology-based laws, Gestalt principles, cognitive load, mental models, onboarding, salience, or decision-making heuristics.
---

Use this skill when the task is fundamentally about choosing or defending design decisions with psychology-backed UX laws.

Keep the skill lean in-context:
- Read [`references/laws-reference.md`](references/laws-reference.md) for the law taxonomy, scenario mapping, compound patterns, and conflict rules.
- Read [`references/source-map.md`](references/source-map.md) only when you need source coverage, URLs, or to refresh the crawl scope.

## Core Approach

Do not dump a catalog of laws. First identify the user's real design problem, then select the smallest useful set of laws.

1. Define the interface problem
- What is the user trying to do?
- Where is the friction: discovery, choice, comprehension, memory, navigation, input, trust, speed, error recovery, or emotional impression?
- What constraints matter: accessibility, responsiveness, engineering cost, novelty, business priority?

2. Classify the problem
- `choice` for too many options, hard comparison, indecision
- `attention` for weak hierarchy, banner blindness, competing stimuli
- `memory` for recall burden, multi-step flows, dense interfaces
- `grouping` for layout organization, scanability, relation between elements
- `learnability` for onboarding, conventions, mental models, redesigns
- `speed` for lag, waiting, excessive interaction cost, slow task completion
- `emotion` for delight, trust, memorable peaks, key endings
- `resilience` for messy input, variable usage paths, edge cases

3. Pick 1 primary law and up to 3 supporting laws
- Prefer a clear primary law that explains the biggest failure mode.
- Add complementary laws only when they change the recommendation.
- If two laws conflict, name the tradeoff explicitly instead of pretending both can be maximized.

4. Turn laws into concrete design moves
- Specify what to add, remove, group, reveal, reorder, prefill, highlight, or defer.
- Tie each recommendation to the affected UI surface: nav, search, cards, pricing, onboarding, forms, dashboards, settings, empty states, notifications.
- Favor recognition over recall, clarity over decoration, and resilient defaults over brittle ideal-user assumptions.

5. Validate
- Explain what to test in usability review, analytics, or experiment design.
- If reviewing an existing UI, point to exact components or flows and identify likely regressions.

## Output Shape

When applying this skill, structure the answer around:
- `Problem`
- `Primary law`
- `Supporting laws`
- `Recommended changes`
- `Tradeoffs`
- `How to validate`

If the user asks for a critique or review, lead with findings, not theory.

## Compound Rules

- Familiarity beats novelty by default. Break conventions only with a clear payoff and a testing plan.
- Simplicity is not abstraction. Reduce complexity, but do not hide critical meaning.
- Progressive reveal is useful only when hidden functionality remains discoverable.
- Salience should be scarce. If everything is emphasized, nothing is emphasized.
- Offload complexity from the user to the system whenever engineering can absorb it safely.
- Perceived speed matters, but fake progress that breaks trust is not acceptable.

## Frequent Design Mappings

- Navigation overload: `Hick's Law`, `Choice Overload`, `Jakob's Law`, `Serial Position Effect`
- Dense content or dashboards: `Chunking`, `Cognitive Load`, `Law of Proximity`, `Law of Common Region`
- Forms and checkout: `Fitts's Law`, `Postel's Law`, `Parkinson's Law`, `Working Memory`
- Onboarding and complex products: `Paradox of the Active User`, `Tesler's Law`, `Mental Model`, `Selective Attention`
- Pricing and comparison: `Choice Overload`, `Von Restorff Effect`, `Pareto Principle`
- Search and findability: `Hick's Law`, `Selective Attention`, `Law of Proximity`, `Jakob's Law`
- Progress and completion: `Goal-Gradient Effect`, `Zeigarnik Effect`, `Peak-End Rule`
- Redesigns or disruptive ideas: `Jakob's Law` balanced against novelty guidance in the article patterns

## Anti-Patterns

- Citing a law without changing the interface.
- Using a law as absolute truth instead of a directional heuristic.
- Applying too many laws and producing contradictory advice.
- Confusing aesthetic polish with usability proof.
- Treating cognitive load only as a visual issue; it is also about task structure and decision burden.

## Source Notes

This skill is grounded in the current `lawsofux.com` site structure that includes:
- 30 law pages
- 8 editorial articles
- top-level `Articles`, `Book`, `Cards`, and `Info` pages

The source map records the exact pages visited during the crawl.
