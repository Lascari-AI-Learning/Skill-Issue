# Implementation Plan

> **Session**: `2025-01-07_agent-skills-presentation_k8m3x9`
> **Status**: Draft
> **Spec**: [./spec.md](./spec.md)
> **Created**: 2025-01-07
> **Updated**: 2025-01-07

---

## Overview

- **Checkpoints**: 6 (0 complete)
- **Total Tasks**: 0

## ⬜ Checkpoint 1: Core Narrative Flow

**Goal**: Create the essential story arc: Title → Problem → Hook → Solution intro. Produces a minimal but complete narrative that could be delivered as a 5-min pitch.

### File Context

| State | File | Status | Description |
|-------|------|--------|-------------|
| Before | `slides/00-title.md` | 📄 exists | Old title slide (What is Claude Code?) |
| Before | `slides/01-what-well-cover.md` | 📄 exists | Old agenda slide |
| Before | `slides/02-about-me.md` | 📄 exists | About me slide (partially relevant) |
| Before | `slides/03-conclusion.md` | 📄 exists | Let's Connect slide |
| After | `slides/00-title.md` | 📝 modified | Updated title: The Skill Issue |
| After | `slides/01-problem-overview.md` | ✨ new | Problem slide with placeholder stats |
| After | `slides/02-about-me.md` | 📝 modified | Updated with hook structure |
| After | `slides/03-the-solution.md` | ✨ new | Transition slide introducing skills |
| After | `slides/99-conclusion.md` | 📄 renamed | Renamed from 03 for ordering |

**Projected Structure**:
```
slides/
├── 00-title.md (modified)
├── 01-problem-overview.md (new)
├── 02-about-me.md (modified)
├── 03-the-solution.md (new)
└── 99-conclusion.md (renamed)
```

### Testing Strategy

**Approach**: Visual verification via dev server

**Verification Steps**:
- [ ] `npm run build:slides`
- [ ] `npm run dev`
- [ ] `Verify slides render correctly at localhost:3030`
- [ ] `Check narrative flow makes sense as a mini-presentation`

---

## ⬜ Checkpoint 2: Problem & Credibility Deep Dive

**Goal**: Flesh out the problem section with Cortex 2026 report data and Ford's credibility hook with real numbers. Complete the 'why should you care' section.

**Prerequisites**: Checkpoints 1

### File Context

| State | File | Status | Description |
|-------|------|--------|-------------|
| Before | `slides/01-problem-overview.md` | 📄 exists | Problem placeholder from CP1 |
| Before | `slides/02-about-me.md` | 📄 exists | About me with hook structure |
| After | `slides/01-the-problem.md` | 📝 modified | Cortex data: 90% adoption, stats |
| After | `slides/02-the-meme.md` | ✨ new | Bell curve meme slide |
| After | `slides/03-about-me.md` | 📄 renamed | Renumbered about-me |
| After | `slides/04-the-hook.md` | ✨ new | Ford's numbers with v-clicks |

**Projected Structure**:
```
slides/
├── 00-title.md
├── 01-the-problem.md
├── 02-the-meme.md
├── 03-about-me.md
├── 04-the-hook.md
├── 05-the-solution.md
└── 99-conclusion.md
```

### Testing Strategy

**Approach**: Visual verification + narrative flow check

**Verification Steps**:
- [ ] `npm run build:slides && npm run dev`
- [ ] `Verify Cortex stats display correctly`
- [ ] `Verify v-clicks work on hook slide`
- [ ] `Check problem → hook → solution flow is compelling`

---

## ⬜ Checkpoint 3: Mental Model & Skills Concept

**Goal**: Explain the junior engineer analogy and introduce skills as the solution. Audience understands WHY skills matter.

**Prerequisites**: Checkpoints 2

### File Context

| State | File | Status | Description |
|-------|------|--------|-------------|
| Before | `slides/05-the-solution.md` | 📄 exists | Basic solution intro |
| After | `slides/05-the-question.md` | ✨ new | What are we doing in 2026? |
| After | `slides/06-mental-model.md` | ✨ new | Junior engineer analogy |
| After | `slides/07-what-is-a-skill.md` | ✨ new | Skills definition slide |

**Projected Structure**:
```
slides/
├── 00-title.md
├── 01-the-problem.md
├── 02-the-meme.md
├── 03-about-me.md
├── 04-the-hook.md
├── 05-the-question.md
├── 06-mental-model.md
├── 07-what-is-a-skill.md
└── 99-conclusion.md
```

### Testing Strategy

**Approach**: Visual verification + concept clarity check

**Verification Steps**:
- [ ] `npm run build:slides && npm run dev`
- [ ] `Verify mental model slide clearly explains the analogy`
- [ ] `Check skills concept is introduced clearly`

---

## ⬜ Checkpoint 4: Skills Deep Dive & Example

**Goal**: Show how skills work technically and walk through a specific example. Audience knows HOW skills work.

**Prerequisites**: Checkpoints 3

### File Context

| State | File | Status | Description |
|-------|------|--------|-------------|
| Before | `slides/07-what-is-a-skill.md` | 📄 exists | Skills definition |
| After | `slides/08-how-skills-work.md` | ✨ new | Technical structure, progressive disclosure |
| After | `slides/09-example-skill.md` | ✨ new | Ford's file tree + specific example |
| After | `slides/10-occams-razor.md` | ✨ new | How to build skills (iterate first) |
| After | `public/skill-tree.png` | ✨ new | Screenshot of Ford's skill directory |

**Projected Structure**:
```
slides/
├── 00-title.md
├── 01-the-problem.md
├── 02-the-meme.md
├── 03-about-me.md
├── 04-the-hook.md
├── 05-the-question.md
├── 06-mental-model.md
├── 07-what-is-a-skill.md
├── 08-how-skills-work.md
├── 09-example-skill.md
├── 10-occams-razor.md
└── 99-conclusion.md
```

### Testing Strategy

**Approach**: Visual verification + technical accuracy check

**Verification Steps**:
- [ ] `npm run build:slides && npm run dev`
- [ ] `Verify technical diagrams/images render`
- [ ] `Check example skill walkthrough is clear (5-7 min content)`

---

## ⬜ Checkpoint 5: Vision & Takeaways

**Goal**: Complete the message with the compound gains vision, realistic expectations (10x myth pushback), key takeaways, and ROI math.

**Prerequisites**: Checkpoints 4

### File Context

| State | File | Status | Description |
|-------|------|--------|-------------|
| After | `slides/11-the-vision.md` | ✨ new | Step out of the loop, 10x myth pushback |
| After | `slides/12-key-takeaways.md` | ✨ new | ROI math, mentality shift |

**Projected Structure**:
```
slides/
├── 00-title.md
├── 01-the-problem.md
├── 02-the-meme.md
├── 03-about-me.md
├── 04-the-hook.md
├── 05-the-question.md
├── 06-mental-model.md
├── 07-what-is-a-skill.md
├── 08-how-skills-work.md
├── 09-example-skill.md
├── 10-occams-razor.md
├── 11-the-vision.md
├── 12-key-takeaways.md
└── 99-conclusion.md
```

### Testing Strategy

**Approach**: Visual verification + message completeness check

**Verification Steps**:
- [ ] `npm run build:slides && npm run dev`
- [ ] `Verify ROI math is clear and compelling`
- [ ] `Check full narrative arc is complete`

---

## ⬜ Checkpoint 6: Polish & Assets

**Goal**: Final polish: update conclusion slide, ensure all images/screenshots are in place, add speaker notes, styling consistency pass.

**Prerequisites**: Checkpoints 5

### File Context

| State | File | Status | Description |
|-------|------|--------|-------------|
| Before | `slides/99-conclusion.md` | 📄 exists | Let's Connect slide |
| After | `slides/99-conclusion.md` | 📝 modified | Updated closing slide |
| After | `public/skill-issue.jpg` | ✨ new | Bell curve meme image |
| After | `public/cortex-stats.png` | ✨ new | Cortex report screenshot |

**Projected Structure**:
```
slides/
├── 00-title.md
├── 01-the-problem.md
├── 02-the-meme.md
├── 03-about-me.md
├── 04-the-hook.md
├── 05-the-question.md
├── 06-mental-model.md
├── 07-what-is-a-skill.md
├── 08-how-skills-work.md
├── 09-example-skill.md
├── 10-occams-razor.md
├── 11-the-vision.md
├── 12-key-takeaways.md
└── 99-conclusion.md (final)
```

### Testing Strategy

**Approach**: Full presentation run-through

**Verification Steps**:
- [ ] `npm run build:slides && npm run dev`
- [ ] `Run through entire presentation`
- [ ] `Verify all images load`
- [ ] `Check speaker notes are helpful`
- [ ] `Verify ~15 min of content`

---

---
*Auto-generated from plan.json on 2026-01-07 13:32*