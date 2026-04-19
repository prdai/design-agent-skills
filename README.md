# html-design

An agent skill for creating polished HTML design artifacts. Built for [skills.sh](https://skills.sh).

Transforms your AI agent into an embodied design expert — slide designer, prototyper, animator, UX designer — producing thoughtful, well-crafted HTML artifacts with real interactions.

## What it does

- **Slide decks** — Fixed-size 1920×1080 HTML presentations with scaling, keyboard nav, localStorage persistence, and speaker notes
- **Interactive prototypes** — Hi-fi clickable mockups with real interactions and a Tweaks panel for live variant toggling
- **Animated videos** — Timeline-based motion design with Stage/Sprite/scrubber patterns
- **Design explorations** — 3+ labeled variants on a design canvas for client/team review
- **Wireframes** — Low-fidelity storyboards to explore ideas quickly

## Workflow

The skill enforces a structured process:

1. **Ask good questions first** — audience, design context, variant count, tweak preferences
2. **Gather design context** — reads existing tokens, theme files, and components before writing a line
3. **Announce the system** — vocalizes layout, color, and type decisions upfront
4. **Build iteratively** — skeleton first, show early, add detail in passes
5. **3+ variants always** — conventional → novel, exposed via a Tweaks panel
6. **Verify in browser** — Playwright screenshots and console error checks before shipping

## Install

```bash
npx skills add prdai/design-agent-skills
```

## Usage

Once installed, the skill activates when you ask your agent to:

- Design, mock up, or prototype a UI
- Create a presentation or slide deck
- Build an animated video or motion design artifact
- Explore design options or create wireframes

## Technical highlights

- Pinned React 18.3.1 + Babel 7.29.0 with integrity hashes (no version drift)
- Named style objects to prevent Babel scope collisions
- `window` exports for cross-file component sharing
- localStorage-persisted state for decks and multi-step flows
- Tweaks panel protocol for live in-page design controls
- `oklch()` color usage for harmonious palettes
- Anti-slop guidelines (no gradient defaults, no emoji, no border-accent cards)

## License

[Apache 2.0](LICENSE)
