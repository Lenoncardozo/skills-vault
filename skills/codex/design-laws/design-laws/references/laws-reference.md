# Design Laws Reference

Use this file when you need the actual law selection logic, scenario mapping, and applied patterns.

## Categories

### Choice and decision

| Law | Use it when | Practical moves | Watch for |
|---|---|---|---|
| Aesthetic-Usability Effect | polish changes user confidence or tolerance | improve visual quality around critical workflows, but keep testing usability | beautiful UI can hide broken flows |
| Choice Overload | users freeze in catalog, pricing, menus, filters | reduce visible options, stage decisions, support side-by-side comparison, front-load recommendations | burying options without search/filter recovery |
| Hick's Law | response time grows with option count and complexity | shorten menus, simplify controls, split flows into steps, highlight recommended choices | oversimplifying until choices become vague |
| Occam's Razor | solutions keep accumulating unnecessary parts | start from the simplest workable interaction, remove assumptions, cut decorative friction | removing too much and losing meaning |
| Pareto Principle | only a small subset drives most value | optimize the most-used paths first, prioritize top tasks, simplify around dominant use cases | ignoring important long-tail workflows |

### Attention, salience, and memory

| Law | Use it when | Practical moves | Watch for |
|---|---|---|---|
| Chunking | content is dense or hard to scan | break information into labeled modules, use hierarchy and spacing, group by intent | arbitrary chunks that do not match user goals |
| Cognitive Bias | users and teams overtrust assumptions or shortcuts | design with awareness of bias, check framing, ranking, defaults, and social proof effects | manipulative nudges or biased interpretation |
| Cognitive Load | people feel overwhelmed or miss details | remove unnecessary processing, cut distractions, simplify tasks, use familiar patterns | treating all complexity as visual only |
| Miller's Law | teams justify seven-item limits or overload short-term memory | group information into meaningful chunks, avoid memory-heavy choices | taking 7 plus/minus 2 as a strict UI rule |
| Selective Attention | key actions are missed because users filter noise | strengthen hierarchy, reduce competing stimuli, avoid ad-like styling, stage changes | banner blindness and change blindness |
| Serial Position Effect | list position affects recall | place high-value items at edges of navs and menus, demote low-value items to the middle | putting all important items in the middle |
| Von Restorff Effect | one action or message must stand out | use contrast, scale, position, or motion sparingly to isolate the key item | over-emphasis, ad-like CTAs, color-only distinction |
| Working Memory | users must remember prior info across screens | persist relevant data, show breadcrumbs and visited states, favor recognition over recall | multi-step flows that force memorization |
| Zeigarnik Effect | you want users to continue unfinished flows | show progress, create clear next steps, expose incomplete states, support resumption | manipulative fake progress without value |

### Grouping and perception

| Law | Use it when | Practical moves | Watch for |
|---|---|---|---|
| Law of Common Region | sections need clear boundaries | use cards, panels, tinted backgrounds, bordered clusters | overboxing everything and flattening hierarchy |
| Law of Proximity | related items are not read as related | adjust spacing to create groups, improve scan paths, cluster metadata with parent items | tight spacing causing false grouping |
| Law of Praegnanz | visuals are harder to parse than necessary | simplify forms, icons, diagrams, and compositions into clearer wholes | stripping nuance users need |
| Law of Similarity | related actions need fast recognition | unify color, shape, size, or behavior to signal same role | styling links or interactive text too similarly to body copy |
| Law of Uniform Connectedness | relation needs stronger proof than proximity alone | connect items with shared frames, lines, arrows, or explicit containers | adding connectors that imply the wrong relationship |

### Familiarity, learning, and onboarding

| Law | Use it when | Practical moves | Watch for |
|---|---|---|---|
| Jakob's Law | redesigns or novel patterns risk disorientation | keep core patterns familiar, preserve stable conventions, offer transition paths during major redesigns | novelty without clear user benefit |
| Mental Model | users import expectations from similar systems | match established domain conventions, use research to close mental-model gaps | designing around the team's model instead of the user's |
| Paradox of the Active User | new users skip tours and start doing | replace long tours with contextual guidance, tooltips, checklists, and progressive onboarding | blocking the product behind education |
| Tesler's Law | inherent complexity must land somewhere | move unavoidable complexity into system logic, defaults, automation, and shared components | abstracting until users lose control or understanding |

### Speed, effort, and task completion

| Law | Use it when | Practical moves | Watch for |
|---|---|---|---|
| Doherty Threshold | lag breaks flow or trust | respond within about 400 ms when possible, use feedback and perceived performance during waits | loading indicators that feel dishonest |
| Fitts's Law | important targets are hard to acquire | enlarge targets, increase spacing, keep actions close to attention area | tiny controls in mobile or dense tables |
| Flow | users should stay immersed in a task | balance challenge with skill, reduce friction, confirm progress, keep discovery available | oversimplifying expert tools into boredom |
| Goal-Gradient Effect | motivation drops before completion | show proximity to completion, grant head starts, expose progress clearly | long forms with no visible progress |
| Parkinson's Law | tasks expand longer than users expect | reduce steps, use autofill and sensible defaults, align duration with expectations | wasting time in obvious administrative work |

### Emotion, recall, and resilience

| Law | Use it when | Practical moves | Watch for |
|---|---|---|---|
| Peak-End Rule | memory of an experience matters as much as execution | design key peak moments and endings carefully, especially success, wait, and recovery states | ignoring negative peaks in error or waiting states |
| Postel's Law | user input and paths are variable or messy | accept flexible input, normalize it safely, set boundaries, give clear error feedback | being permissive without clear constraints |

## Scenario Mapping

### Navigation and information architecture

- Start with `Hick's Law` and `Choice Overload` when menus feel dense.
- Use `Serial Position Effect` to place highest-value destinations at edges.
- Use `Jakob's Law` before inventing new nav patterns.
- Use `Law of Proximity` and `Law of Common Region` to show grouping.

### Search, results, and discovery

- Use `Hick's Law` to simplify initial search actions.
- Use `Selective Attention` to make the query box, suggestions, and result hierarchy obvious.
- Use `Law of Proximity` to group title, metadata, and snippet per result.
- Use `Law of Uniform Connectedness` or subtle cards to elevate special result types.

### Forms, checkout, and data entry

- Use `Fitts's Law` for target size and spacing.
- Use `Postel's Law` for flexible, resilient input parsing.
- Use `Working Memory` to persist important information between steps.
- Use `Parkinson's Law` to cut time with autofill, defaults, and reduced friction.
- Use `Goal-Gradient Effect` to show progress and completion distance.

### Onboarding and complex products

- Default to `Paradox of the Active User`: let people start first.
- Use `Tesler's Law` to absorb complexity in system design instead of training users to cope.
- Use `Mental Model` to anchor the experience in known patterns.
- Use `Selective Attention` to reveal only what matters now.
- Use `Chunking` for initial setup and learning surfaces.

### Pricing, plan selection, and comparison

- `Choice Overload` limits how many plans or variants should be surfaced at once.
- `Von Restorff Effect` can isolate a recommended tier.
- `Pareto Principle` helps focus comparison around the few differences that matter.
- Use explicit side-by-side comparison to reduce decision friction.

### Dashboards, dense views, and content-heavy surfaces

- `Chunking`, `Law of Proximity`, `Law of Common Region`, and `Law of Similarity` are the main structure tools.
- `Cognitive Load` should govern every extra chart, metric, and control.
- `Selective Attention` matters when real-time changes compete for focus.

### Success states, waiting states, and memorable journeys

- `Peak-End Rule` should shape confirmation, summary, completion, and recovery moments.
- `Doherty Threshold` shapes system responsiveness and perceived speed.
- `Zeigarnik Effect` and `Goal-Gradient Effect` support resumable progress.

## Compound Patterns from the Editorial Articles

### Familiarity vs novelty

Default to familiarity because users import expectations from other products. Break conventions only when one of these is true:
- differentiation is a strategic objective
- a new technology genuinely changes the interaction model
- exploration, surprise, or immersion is the goal

If you choose novelty:
- preserve a stable mental model where possible
- keep the novel move local, not everywhere
- user-test the unfamiliar interaction early
- never spend usability capital for superficial brand theater

### Active-user onboarding

People want to start, not study. Prefer:
- contextual tooltips
- progressive onboarding
- guided templates or checklists
- task-based learning in a low-risk environment

Avoid:
- modal slide tours that block product access
- front-loading every feature before first value
- explanations detached from context of use

### Complexity transfer

From the Tesler material:
- some complexity is irreducible
- the question is who bears it
- bias toward making the system do more work than the user

Healthy transfers:
- sensible defaults
- autofill and precomputation
- reusable components and shared interaction patterns
- automation that preserves clarity and reversibility

Unhealthy transfers:
- hiding system rules the user still needs to understand
- abstraction without recoverability
- magic behavior that breaks trust

### Reducing cognitive load

Common causes called out in the site material:
- too many choices
- too much thought required
- lack of clarity

Reliable reductions:
- remove unnecessary elements
- use familiar patterns
- eliminate nonessential tasks
- minimize simultaneous choices
- show related choices together
- improve readability and scanability

### Search as a model surface

The Google Search article reinforces a useful pattern:
- a single dominant task
- minimal landing-page clutter
- default focus on the primary field
- predictive assistance that saves keystrokes and mental effort
- strong grouping and scanability in results

Use this pattern when the product has one obvious high-frequency action.

### Designing endings

Peak moments and endings disproportionately shape memory.
- Treat confirmation states as product moments, not bookkeeping.
- Reduce negative peaks during waiting, cancellation, and error recovery.
- Design the post-task state, not just the task itself.

## Conflict Resolution

### Simplicity vs clarity

- Prefer clarity when a simpler option obscures meaning.
- Prefer simplicity when extra UI adds processing but not understanding.

### Familiarity vs novelty

- Familiarity wins for critical flows, broad audiences, and established domains.
- Novelty can win for branded experiences, immersive storytelling, or genuine product differentiation.

### Progressive reveal vs discoverability

- Hide complexity only if users can still find advanced functionality when they need it.
- Use prompts, empty states, templates, and contextual cues to keep features discoverable.

### Salience vs distraction

- Emphasize one thing per region or moment.
- If multiple items seem equally urgent, reduce emphasis and re-establish hierarchy.

### Speed vs trust

- Optimize real speed first.
- Use loaders, skeletons, and animation to preserve continuity, not to disguise poor systems.
- Small deliberate delays are acceptable only when they increase perceived reliability in sensitive moments.

## Review Checklist

Use this quick audit when the user asks for critique:

- Is the primary task obvious within 5 seconds?
- Are there too many visible choices at once?
- Does the layout group related information correctly?
- Are important actions large, close, and easy to hit?
- Is any step relying on memory instead of recognition?
- Are onboarding and guidance embedded in context?
- Are there obvious negative peaks in wait, error, or completion states?
- Is the interface borrowing stable conventions from the category?
- Is visual emphasis scarce and meaningful?
- Has complexity been removed, relocated, or merely hidden?
