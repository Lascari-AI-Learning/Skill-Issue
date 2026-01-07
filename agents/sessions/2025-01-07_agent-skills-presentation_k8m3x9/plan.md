# Implementation Plan

> **Session**: `2025-01-07_agent-skills-presentation_k8m3x9`
> **Status**: Complete
> **Spec**: [./spec.md](./spec.md)
> **Created**: 2025-01-07
> **Updated**: 2025-01-07

---

## Overview

- **Checkpoints**: 6 (0 complete)
- **Total Tasks**: 28

## ✅ Checkpoint 1: Core Narrative Flow

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

### ⬜ Task Group 1.1: Update Title Slide

**Objective**: Transform the title from 'What is Claude Code?' to 'The Skill Issue' with proper subtitle and QR code

#### ⬜ Task 1.1.1: Update title slide content

**File**: `slides/00-title.md`

**Description**: Change the presentation title to 'The Skill Issue', update subtitle to 'Agents Decoded in 2026', update or remove the QR code link, and update speaker notes for the new opening hook.

**Context to Load**:
- `slides/00-title.md` (lines all) - Understand current title slide structure and layout slot syntax
- `agents/sessions/2025-01-07_agent-skills-presentation_k8m3x9/spec.md` (lines 159-165) - Get exact title and subtitle text from spec

**Actions**:
- ⬜ **1.1.1.1**: UPDATE ::title:: slot: REPLACE 'What is Claude Code?' with 'The Skill Issue' (`slides/00-title.md`)
- ⬜ **1.1.1.2**: UPDATE ::subtitle:: slot: REPLACE '...and Why You Should Care' with 'Agents Decoded in 2026' (`slides/00-title.md`)
- ⬜ **1.1.1.3**: UPDATE link frontmatter: REPLACE with presentation-specific link or REMOVE if not needed (`slides/00-title.md`)
- ⬜ **1.1.1.4**: UPDATE speaker notes: REPLACE with opening hook notes about 'cutting through the hype' and 'real value vs Twitter demos' (`slides/00-title.md`)

### ⬜ Task Group 1.2: Create Problem Overview Slide

**Objective**: New slide introducing the core problem (placeholder for Cortex data) - sets up 'why this matters'

#### ⬜ Task 1.2.1: Create problem overview slide

**File**: `slides/01-problem-overview.md`

**Description**: Create a new slide introducing the gap between AI coding demos and production reality. Include placeholder for Cortex 2026 stats (90% adoption), the productivity paradox concept, and 'AI amplifies whatever you have' theme.

**Context to Load**:
- `agents/sessions/2025-01-07_agent-skills-presentation_k8m3x9/spec.md` (lines 167-184) - Get problem section content from spec outline
- `slides/00-title.md` (lines all) - Reference frontmatter structure and styling

**Depends On**: Tasks 1.1.1

**Actions**:
- ⬜ **1.2.1.1**: CREATE FILE slides/01-problem-overview.md with frontmatter (theme: ../, layout: default) (`slides/01-problem-overview.md`)
- ⬜ **1.2.1.2**: ADD headline: 'The Problem' centered at top (`slides/01-problem-overview.md`)
- ⬜ **1.2.1.3**: ADD bullet points: 90% AI adoption (placeholder), productivity paradox intro, 'AI amplifies whatever you have' (`slides/01-problem-overview.md`)
- ⬜ **1.2.1.4**: ADD speaker notes explaining Cortex report context and 'more code, more bugs' theme (`slides/01-problem-overview.md`)

### ⬜ Task Group 1.3: Update About Me with Hook Structure

**Objective**: Restructure about-me to include the 'proof of real value' hook with placeholders for numbers

#### ⬜ Task 1.3.1: Restructure about-me slide with hook

**File**: `slides/02-about-me.md`

**Description**: Update the about-me slide to include the credibility hook with v-clicks for dramatic reveal. Keep core bio (Applied AI Engineer, 3 years GenAI) but add the 'Why should you trust me?' section with Ford's numbers: +114,427 lines, ~$864 tokens, $23,480 income. End with '95% of the code was written by AI' kicker.

**Context to Load**:
- `slides/02-about-me.md` (lines all) - Understand current about-me structure and speaker layout
- `agents/sessions/2025-01-07_agent-skills-presentation_k8m3x9/spec.md` (lines 186-195) - Get hook structure and exact numbers from spec

**Depends On**: Tasks 1.2.1

**Actions**:
- ⬜ **1.3.1.1**: UPDATE about-me section: Keep core info (Applied AI Engineer, 3 years GenAI, 30+ projects) (`slides/02-about-me.md`)
- ⬜ **1.3.1.2**: ADD hook section with v-clicks: 'Why should you trust me?' (`slides/02-about-me.md`)
- ⬜ **1.3.1.3**: ADD v-click item 1: Line count (+114,427 lines added) (`slides/02-about-me.md`)
- ⬜ **1.3.1.4**: ADD v-click item 2: Token spend (~$864 in Claude Code) (`slides/02-about-me.md`)
- ⬜ **1.3.1.5**: ADD v-click item 3: Income ($23,480 December) (`slides/02-about-me.md`)
- ⬜ **1.3.1.6**: ADD kicker line: '95% of the code was written by AI' (`slides/02-about-me.md`)
- ⬜ **1.3.1.7**: UPDATE speaker notes: Emphasize 'this is not a flex, it is proof of real value' (`slides/02-about-me.md`)

### ⬜ Task Group 1.4: Create Solution Transition Slide

**Objective**: Quick transition slide that pivots from problem to 'the answer is skills'

#### ⬜ Task 1.4.1: Create solution transition slide

**File**: `slides/03-the-solution.md`

**Description**: Create a brief transition slide that pivots from the problem/hook section to introducing skills as the solution. This is a pivot point, not a detailed explanation - that comes in CP3.

**Context to Load**:
- `agents/sessions/2025-01-07_agent-skills-presentation_k8m3x9/spec.md` (lines 220-223) - Get solution section intro from spec
- `slides/00-title.md` (lines 1-6) - Reference frontmatter structure

**Depends On**: Tasks 1.3.1

**Actions**:
- ⬜ **1.4.1.1**: CREATE FILE slides/03-the-solution.md with frontmatter (theme: ../, layout: default) (`slides/03-the-solution.md`)
- ⬜ **1.4.1.2**: ADD headline: 'What is the Answer?' or 'The Solution' centered (`slides/03-the-solution.md`)
- ⬜ **1.4.1.3**: ADD teaser content: 'Skills - encoding your engineering expertise for AI agents' (`slides/03-the-solution.md`)
- ⬜ **1.4.1.4**: ADD speaker notes: Brief transition explanation, sets up skills deep dive (`slides/03-the-solution.md`)

### ⬜ Task Group 1.5: Reorganize File Structure

**Objective**: Rename conclusion slide to 99-conclusion.md, delete obsolete slides, run build:slides

#### ⬜ Task 1.5.1: Rename conclusion slide

**File**: `slides/03-conclusion.md`

**Description**: Move the conclusion/Let's Connect slide to slides/99-conclusion.md so it appears at the end of the presentation ordering.

**Context to Load**:
- `slides/03-conclusion.md` (lines all) - Verify file exists and content is correct before moving

**Depends On**: Tasks 1.4.1

**Actions**:
- ⬜ **1.5.1.1**: MOVE slides/03-conclusion.md to slides/99-conclusion.md (`slides/03-conclusion.md`)

#### ⬜ Task 1.5.2: Delete obsolete agenda slide

**File**: `slides/01-what-well-cover.md`

**Description**: Remove the old 'What We'll Cover' agenda slide that no longer fits the new presentation narrative.

**Depends On**: Tasks 1.5.1

**Actions**:
- ⬜ **1.5.2.1**: DELETE slides/01-what-well-cover.md (`slides/01-what-well-cover.md`)

#### ⬜ Task 1.5.3: Build and verify slides

**File**: `None`

**Description**: Run the build script to regenerate index.md and verify all slides render correctly via the dev server.

**Depends On**: Tasks 1.5.2

**Actions**:
- ⬜ **1.5.3.1**: RUN npm run build:slides to regenerate index.md from slides directory
- ⬜ **1.5.3.2**: RUN npm run dev to start dev server and verify slides render at localhost:3030

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

### ⬜ Task Group 2.1: Expand Problem Slide with Cortex Data

**Objective**: Add the full Cortex 2026 stats (90% adoption, PRs +20%, incidents +23.5%, change failure +30%)

#### ⬜ Task 2.1.1: Expand problem slide with Cortex statistics

**File**: `slides/01-the-problem.md`

**Description**: Rename slides/01-problem-overview.md to slides/01-the-problem.md and expand with full Cortex 2026 data: 90% adoption headline, productivity paradox stats (PRs +20%, Incidents +23.5%, Change failure +30%), and 'AI amplifies whatever you have' conclusion.

**Context to Load**:
- `slides/01-problem-overview.md` (lines all) - Get current placeholder content to expand
- `agents/sessions/2025-01-07_agent-skills-presentation_k8m3x9/spec.md` (lines 167-184) - Get full Cortex data and problem section details

**Actions**:
- ⬜ **2.1.1.1**: RENAME slides/01-problem-overview.md to slides/01-the-problem.md (`slides/01-problem-overview.md`)
- ⬜ **2.1.1.2**: UPDATE content: ADD Cortex 2026 headline '90% adoption, zero standardization' (`slides/01-the-problem.md`)
- ⬜ **2.1.1.3**: ADD stats grid: PRs per author +20%, Incidents per PR +23.5%, Change failure rate +30% (`slides/01-the-problem.md`)
- ⬜ **2.1.1.4**: UPDATE speaker notes with full Cortex report context and link (`slides/01-the-problem.md`)

### ⬜ Task Group 2.2: Create Bell Curve Meme Slide

**Objective**: The 'skill issue' meme - left: let AI write code, middle: crying, right: let AI write code

#### ⬜ Task 2.2.1: Create skill issue meme slide

**File**: `slides/02-the-meme.md`

**Description**: Create a new slide featuring the bell curve meme (skill-issue.jpg). Left side: 'Let AI Write the Code', Middle (crying): 'AI Cannot Match My Skills', Right (enlightened): 'Let AI Write the Code'. Include speaker notes about the reframe.

**Context to Load**:
- `agents/sessions/2025-01-07_agent-skills-presentation_k8m3x9/spec.md` (lines 179-184) - Get meme structure and messaging from spec

**Depends On**: Tasks 2.1.1

**Actions**:
- ⬜ **2.2.1.1**: CREATE FILE slides/02-the-meme.md with frontmatter (theme: ../, layout: default) (`slides/02-the-meme.md`)
- ⬜ **2.2.1.2**: ADD bell curve meme image placeholder: img src /skill-issue.jpg (`slides/02-the-meme.md`)
- ⬜ **2.2.1.3**: ADD caption text for bell curve: Left 'Let AI Write the Code', Middle 'AI Cannot Match My Skills', Right 'Let AI Write the Code' (`slides/02-the-meme.md`)
- ⬜ **2.2.1.4**: ADD speaker notes: 'Everyone has seen this meme' + reframe: for skilled engineers AI is a HUGE force multiplier (`slides/02-the-meme.md`)

### ⬜ Task Group 2.3: Add Personal Anecdote

**Objective**: Ford's story about the bad client project with 5000-line files

#### ⬜ Task 2.3.1: Add personal anecdote to problem slide

**File**: `slides/01-the-problem.md`

**Description**: Add Ford's personal anecdote to the problem slide: recent client project, UI engineer using Cursor without understanding, 5000+ line files, hardcoded strings, 20 components per file. Key message: 'Not his fault - he didn't know what he was doing'.

**Context to Load**:
- `slides/01-the-problem.md` (lines all) - See current state after Cortex data expansion
- `agents/sessions/2025-01-07_agent-skills-presentation_k8m3x9/spec.md` (lines 173-178) - Get anecdote details from spec

**Depends On**: Tasks 2.1.1

**Actions**:
- ⬜ **2.3.1.1**: ADD section: 'I have seen this firsthand' with personal anecdote (`slides/01-the-problem.md`)
- ⬜ **2.3.1.2**: ADD details: client project, UI engineer + Cursor, 5000+ line files, hardcoded strings, 20 components per file (`slides/01-the-problem.md`)
- ⬜ **2.3.1.3**: ADD lesson: 'Not his fault - he did not know what he was doing' (`slides/01-the-problem.md`)

### ⬜ Task Group 2.4: Separate Hook into Own Slide

**Objective**: Extract the dramatic reveal (numbers) into its own slide with v-clicks

#### ⬜ Task 2.4.1: Create dedicated hook slide with v-clicks

**File**: `slides/04-the-hook.md`

**Description**: Create a new slide dedicated to the dramatic reveal of Ford's numbers. Use v-clicks to reveal: 1) Line count (+114,427), 2) Token spend (~$864), 3) Income ($23,480 December). End with kicker: '95% of the code was written by AI'.

**Context to Load**:
- `slides/02-about-me.md` (lines all) - Get hook content to extract
- `agents/sessions/2025-01-07_agent-skills-presentation_k8m3x9/spec.md` (lines 186-195) - Get exact numbers and hook structure

**Depends On**: Tasks 2.3.1

**Actions**:
- ⬜ **2.4.1.1**: CREATE FILE slides/04-the-hook.md with frontmatter (`slides/04-the-hook.md`)
- ⬜ **2.4.1.2**: ADD headline: 'Why should you trust me?' or 'The Proof' (`slides/04-the-hook.md`)
- ⬜ **2.4.1.3**: ADD v-click 1: Line count (+114,427 lines added) with visual styling (`slides/04-the-hook.md`)
- ⬜ **2.4.1.4**: ADD v-click 2: Token spend (~$864 in Claude Code) (`slides/04-the-hook.md`)
- ⬜ **2.4.1.5**: ADD v-click 3: Income ($23,480 December) (`slides/04-the-hook.md`)
- ⬜ **2.4.1.6**: ADD kicker with v-click: '95% of the code was written by AI' (`slides/04-the-hook.md`)
- ⬜ **2.4.1.7**: ADD speaker notes: 'This is not a flex - it is proof of real value' (`slides/04-the-hook.md`)

#### ⬜ Task 2.4.2: Update about-me slide and renumber

**File**: `slides/03-about-me.md`

**Description**: Rename slides/02-about-me.md to slides/03-about-me.md. Remove the hook section (now in 04-the-hook.md) and keep only the core bio content.

**Context to Load**:
- `slides/02-about-me.md` (lines all) - Identify what to keep vs remove

**Depends On**: Tasks 2.4.1

**Actions**:
- ⬜ **2.4.2.1**: RENAME slides/02-about-me.md to slides/03-about-me.md (`slides/02-about-me.md`)
- ⬜ **2.4.2.2**: REMOVE hook section from about-me (moved to 04-the-hook.md) (`slides/03-about-me.md`)
- ⬜ **2.4.2.3**: KEEP core bio: Applied AI Engineer, 3 years GenAI, 30+ projects (`slides/03-about-me.md`)

### ⬜ Task Group 2.5: Renumber & Build

**Objective**: Renumber solution slide for proper flow, run build:slides

#### ⬜ Task 2.5.1: Renumber solution slide and build

**File**: `slides/05-the-solution.md`

**Description**: Rename slides/03-the-solution.md to slides/05-the-solution.md for proper ordering after the hook slide. Run build:slides and dev server to verify.

**Depends On**: Tasks 2.4.2

**Actions**:
- ⬜ **2.5.1.1**: RENAME slides/03-the-solution.md to slides/05-the-solution.md (`slides/03-the-solution.md`)
- ⬜ **2.5.1.2**: RUN npm run build:slides to regenerate index.md
- ⬜ **2.5.1.3**: RUN npm run dev to verify slides render correctly

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

### ⬜ Task Group 3.1: Create The Question Slide

**Objective**: Transition slide: 'What are we doing in 2026 to fix this?'

#### ⬜ Task 3.1.1: Create the question slide

**File**: `slides/05-the-question.md`

**Description**: Create a transition slide that pivots from the problem/hook to the solution. Content: 'Now that we've defined the problem... What are we doing in 2026 to fix this? What should you allocate your time and resources to? How do you build TRUST into your AI system?'

**Context to Load**:
- `agents/sessions/2025-01-07_agent-skills-presentation_k8m3x9/spec.md` (lines 197-201) - Get the question slide content from spec

**Actions**:
- ⬜ **3.1.1.1**: RENAME slides/05-the-solution.md to slides/06-the-solution.md to make room (`slides/05-the-solution.md`)
- ⬜ **3.1.1.2**: CREATE FILE slides/05-the-question.md with frontmatter (`slides/05-the-question.md`)
- ⬜ **3.1.1.3**: ADD content: 'What are we doing in 2026?', 'What should you allocate time/resources to?', 'How do you build TRUST?' (`slides/05-the-question.md`)
- ⬜ **3.1.1.4**: ADD speaker notes: This is the pivot moment, set up the mental model (`slides/05-the-question.md`)

### ⬜ Task Group 3.2: Create Mental Model Slide

**Objective**: Junior engineer analogy, standardization (commit rules, tests, docs)

#### ⬜ Task 3.2.1: Create mental model slide

**File**: `slides/06-mental-model.md`

**Description**: Create slide explaining the junior engineer analogy: 'This isn't new - every engineering team already does this'. Cover: determining tasks, handing off, reviewing PRs, implicit/explicit standardization (commit rules, tests, GitHub Actions, company protocols, documentation).

**Context to Load**:
- `agents/sessions/2025-01-07_agent-skills-presentation_k8m3x9/spec.md` (lines 203-217) - Get mental model content from spec

**Depends On**: Tasks 3.1.1

**Actions**:
- ⬜ **3.2.1.1**: RENAME slides/06-the-solution.md to slides/08-the-solution.md to make room for new slides (`slides/06-the-solution.md`)
- ⬜ **3.2.1.2**: CREATE FILE slides/06-mental-model.md with frontmatter (`slides/06-mental-model.md`)
- ⬜ **3.2.1.3**: ADD headline: 'This Isn't New' or 'The Mental Model' (`slides/06-mental-model.md`)
- ⬜ **3.2.1.4**: ADD junior engineer workflow: determine task -> hand off -> review PR -> HOW is not controlled (`slides/06-mental-model.md`)
- ⬜ **3.2.1.5**: ADD standardization list: commit rules, tests must pass, GitHub Actions, company protocols, documentation (`slides/06-mental-model.md`)
- ⬜ **3.2.1.6**: ADD key insight: 'Same docs you would give a new junior = what you give the LLM' (`slides/06-mental-model.md`)
- ⬜ **3.2.1.7**: ADD speaker notes explaining the analogy (`slides/06-mental-model.md`)

### ⬜ Task Group 3.3: Create What Is A Skill Slide

**Objective**: Skills definition, Anthropic structure, self-discovery

#### ⬜ Task 3.3.1: Create what is a skill slide

**File**: `slides/07-what-is-a-skill.md`

**Description**: Create slide defining what skills are: opinionated way of formatting Markdown files, allows agent to self-discover processes, Anthropic recently released this as standard structure, not complicated to set up.

**Context to Load**:
- `agents/sessions/2025-01-07_agent-skills-presentation_k8m3x9/spec.md` (lines 219-223) - Get skills definition from spec

**Depends On**: Tasks 3.2.1

**Actions**:
- ⬜ **3.3.1.1**: CREATE FILE slides/07-what-is-a-skill.md with frontmatter (`slides/07-what-is-a-skill.md`)
- ⬜ **3.3.1.2**: ADD headline: 'What is a Skill?' (`slides/07-what-is-a-skill.md`)
- ⬜ **3.3.1.3**: ADD bullet: Skills = opinionated way of formatting Markdown files (`slides/07-what-is-a-skill.md`)
- ⬜ **3.3.1.4**: ADD bullet: Allows agent to SELF-DISCOVER processes within the skill (`slides/07-what-is-a-skill.md`)
- ⬜ **3.3.1.5**: ADD bullet: Anthropic recently released this, becoming the standard structure (`slides/07-what-is-a-skill.md`)
- ⬜ **3.3.1.6**: ADD bullet: Not that complicated to set up (`slides/07-what-is-a-skill.md`)
- ⬜ **3.3.1.7**: ADD speaker notes about skills background (`slides/07-what-is-a-skill.md`)

### ⬜ Task Group 3.4: Build & Verify

**Objective**: Run build:slides and verify

#### ⬜ Task 3.4.1: Build and verify CP3 slides

**File**: `None`

**Description**: Run build:slides to regenerate index.md and verify all slides render correctly.

**Depends On**: Tasks 3.3.1

**Actions**:
- ⬜ **3.4.1.1**: RUN npm run build:slides
- ⬜ **3.4.1.2**: RUN npm run dev and verify slides 05-07 render correctly

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

### ⬜ Task Group 4.1: Create How Skills Work Slide

**Objective**: File structure, progressive disclosure, prompt appearance

#### ⬜ Task 4.1.1: Create how skills work slide

**File**: `slides/08-how-skills-work.md`

**Description**: Create slide showing how skills work technically: top-level structure, how it appears in the prompt (model sees skills available, thinks 'I need to acquire this skill', reads skill files, knowledge is now in context), file tree structure (SKILL.md, references/), progressive disclosure concept.

**Context to Load**:
- `agents/sessions/2025-01-07_agent-skills-presentation_k8m3x9/spec.md` (lines 225-236) - Get how skills work content from spec

**Actions**:
- ⬜ **4.1.1.1**: RENAME slides/08-the-solution.md to DELETE (this slide is now obsolete) (`slides/08-the-solution.md`)
- ⬜ **4.1.1.2**: CREATE FILE slides/08-how-skills-work.md with frontmatter (`slides/08-how-skills-work.md`)
- ⬜ **4.1.1.3**: ADD headline: 'How Skills Work' (`slides/08-how-skills-work.md`)
- ⬜ **4.1.1.4**: ADD prompt flow: Model sees skills -> thinks 'I need this skill' -> reads skill files -> knowledge in context (`slides/08-how-skills-work.md`)
- ⬜ **4.1.1.5**: ADD file tree structure: SKILL.md (main file), references/ (linked docs) (`slides/08-how-skills-work.md`)
- ⬜ **4.1.1.6**: ADD key concept: Progressive disclosure - only load context when needed (`slides/08-how-skills-work.md`)
- ⬜ **4.1.1.7**: ADD speaker notes about technical implementation (`slides/08-how-skills-work.md`)

### ⬜ Task Group 4.2: Create Example Skill Slide

**Objective**: Ford's file tree, specific skill walkthrough

#### ⬜ Task 4.2.1: Create example skill slide

**File**: `slides/09-example-skill.md`

**Description**: Create slide showing Ford's Claude Code config file tree and a specific skill walkthrough. Include image placeholder for public/skill-tree.png. Note: 'This isn't comprehensive - this is how I work'.

**Context to Load**:
- `agents/sessions/2025-01-07_agent-skills-presentation_k8m3x9/spec.md` (lines 251-265) - Get example skill content from spec

**Depends On**: Tasks 4.1.1

**Actions**:
- ⬜ **4.2.1.1**: CREATE FILE slides/09-example-skill.md with frontmatter (`slides/09-example-skill.md`)
- ⬜ **4.2.1.2**: ADD headline: 'Example: My Skills Setup' (`slides/09-example-skill.md`)
- ⬜ **4.2.1.3**: ADD image placeholder for skill-tree.png showing Ford's Claude Code config (`slides/09-example-skill.md`)
- ⬜ **4.2.1.4**: ADD caption: 'I have a lot of skills/commands built out - this is how I work' (`slides/09-example-skill.md`)
- ⬜ **4.2.1.5**: ADD specific skill walkthrough section (TBD which skill) (`slides/09-example-skill.md`)
- ⬜ **4.2.1.6**: ADD speaker notes: 5-7 min for skills section, light touch (`slides/09-example-skill.md`)

### ⬜ Task Group 4.3: Create Occam's Razor Slide

**Objective**: How to build skills: work in the loop first, then step out

#### ⬜ Task 4.3.1: Create Occam's razor slide

**File**: `slides/10-occams-razor.md`

**Description**: Create slide about the right approach to building skills: Common mistake (give everything to agent right away), Right approach (work IN the loop first, iterate until happy, THEN figure out how to step out), Keep it simple.

**Context to Load**:
- `agents/sessions/2025-01-07_agent-skills-presentation_k8m3x9/spec.md` (lines 254-264) - Get Occam's razor content from spec

**Depends On**: Tasks 4.2.1

**Actions**:
- ⬜ **4.3.1.1**: CREATE FILE slides/10-occams-razor.md with frontmatter (`slides/10-occams-razor.md`)
- ⬜ **4.3.1.2**: ADD headline: 'Building Skills: Occam's Razor' (`slides/10-occams-razor.md`)
- ⬜ **4.3.1.3**: ADD common mistake: giving everything to agent right out the gate -> leads to bad skills (`slides/10-occams-razor.md`)
- ⬜ **4.3.1.4**: ADD right approach: Work IN the loop first -> Iterate until happy -> THEN step out (`slides/10-occams-razor.md`)
- ⬜ **4.3.1.5**: ADD key principle: Keep it as simple as possible - don't add complexity until you need it (`slides/10-occams-razor.md`)
- ⬜ **4.3.1.6**: ADD speaker notes about simplicity principle (`slides/10-occams-razor.md`)

### ⬜ Task Group 4.4: Build & Verify

**Objective**: Run build:slides and verify

#### ⬜ Task 4.4.1: Build and verify CP4 slides

**File**: `None`

**Description**: Run build:slides to regenerate index.md and verify all slides render correctly.

**Depends On**: Tasks 4.3.1

**Actions**:
- ⬜ **4.4.1.1**: RUN npm run build:slides
- ⬜ **4.4.1.2**: RUN npm run dev and verify slides 08-10 render correctly

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

### ⬜ Task Group 5.1: Create Vision Slide

**Objective**: Step out of loop, 10x myth pushback

#### ⬜ Task 5.1.1: Create the vision slide

**File**: `slides/11-the-vision.md`

**Description**: Create slide about the compound gains vision: What we're doing with skills = encoding your engineering knowledge, First agent does flows you already do efficiently, Then trust builds -> queue as background task -> just review, Goal: step farther and farther out of the loop. Include 10x myth pushback: Reality is 10% faster here, 5% faster there, compounds over MONTHS.

**Context to Load**:
- `agents/sessions/2025-01-07_agent-skills-presentation_k8m3x9/spec.md` (lines 238-249) - Get vision content from spec

**Actions**:
- ⬜ **5.1.1.1**: CREATE FILE slides/11-the-vision.md with frontmatter (`slides/11-the-vision.md`)
- ⬜ **5.1.1.2**: ADD headline: 'The Vision' or 'Where We're Headed' (`slides/11-the-vision.md`)
- ⬜ **5.1.1.3**: ADD progression: Skills = encoding knowledge -> agent does your flows -> trust builds -> background tasks -> just review (`slides/11-the-vision.md`)
- ⬜ **5.1.1.4**: ADD 10x myth pushback: NOT instant transformation, Reality: 10% here, 5% there, compounds over MONTHS (`slides/11-the-vision.md`)
- ⬜ **5.1.1.5**: ADD key message: No magic pill - AI does NOT replace knowledge, you're building TOWARDS that future (`slides/11-the-vision.md`)
- ⬜ **5.1.1.6**: ADD speaker notes about realistic expectations (`slides/11-the-vision.md`)

### ⬜ Task Group 5.2: Create Key Takeaways Slide

**Objective**: ROI math ($10K → $40K), mentality shift

#### ⬜ Task 5.2.1: Create key takeaways slide

**File**: `slides/12-key-takeaways.md`

**Description**: Create slide with key takeaways: Don't let bad examples blind you, For skilled engineers AI is huge force multiplier, THE MATH: $1K/month tokens x 10 engineers = $10K, average engineer costs $10K, 40% more effective = $40K value, spend $10K to get $40K = 4x ROI. The mentality: What can we systematize into skills?

**Context to Load**:
- `agents/sessions/2025-01-07_agent-skills-presentation_k8m3x9/spec.md` (lines 267-280) - Get key takeaways content from spec

**Depends On**: Tasks 5.1.1

**Actions**:
- ⬜ **5.2.1.1**: CREATE FILE slides/12-key-takeaways.md with frontmatter (`slides/12-key-takeaways.md`)
- ⬜ **5.2.1.2**: ADD headline: 'Key Takeaways' (`slides/12-key-takeaways.md`)
- ⬜ **5.2.1.3**: ADD takeaway 1: Don't let bad examples blind you - this is coming (`slides/12-key-takeaways.md`)
- ⬜ **5.2.1.4**: ADD takeaway 2: For skilled engineers, AI is a HUGE force multiplier (`slides/12-key-takeaways.md`)
- ⬜ **5.2.1.5**: ADD ROI math: $1K tokens x 10 engineers = $10K spend, 40% more effective = $40K value, 4x ROI (`slides/12-key-takeaways.md`)
- ⬜ **5.2.1.6**: ADD mentality shift: What can we systematize into skills? Transfer best practices to whole team (`slides/12-key-takeaways.md`)
- ⬜ **5.2.1.7**: ADD closing: Skills = encoding knowledge -> compound gains over time (`slides/12-key-takeaways.md`)
- ⬜ **5.2.1.8**: ADD speaker notes with emphasis on the math being a no-brainer (`slides/12-key-takeaways.md`)

### ⬜ Task Group 5.3: Build & Verify

**Objective**: Run build:slides and verify full narrative

#### ⬜ Task 5.3.1: Build and verify CP5 slides

**File**: `None`

**Description**: Run build:slides and verify the full narrative arc is complete.

**Depends On**: Tasks 5.2.1

**Actions**:
- ⬜ **5.3.1.1**: RUN npm run build:slides
- ⬜ **5.3.1.2**: RUN npm run dev and verify complete narrative flow

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

### ⬜ Task Group 6.1: Update Conclusion Slide

**Objective**: Verify Let's Connect QR codes work

#### ⬜ Task 6.1.1: Verify and update conclusion slide

**File**: `slides/99-conclusion.md`

**Description**: Verify the Let's Connect slide has correct QR codes for X, LinkedIn, and Website. Update the closing message to match the presentation theme. Ensure 'Questions?' prompt is present.

**Context to Load**:
- `slides/99-conclusion.md` (lines all) - Review current conclusion slide content
- `agents/sessions/2025-01-07_agent-skills-presentation_k8m3x9/spec.md` (lines 281-284) - Get conclusion section from spec

**Actions**:
- ⬜ **6.1.1.1**: VERIFY QR codes for X, LinkedIn, Website are correct and working (`slides/99-conclusion.md`)
- ⬜ **6.1.1.2**: UPDATE closing message to match presentation theme if needed (`slides/99-conclusion.md`)
- ⬜ **6.1.1.3**: UPDATE speaker notes with closing remarks (`slides/99-conclusion.md`)

### ⬜ Task Group 6.2: Add Missing Assets

**Objective**: skill-issue.jpg, cortex-stats.png, skill-tree.png

#### ⬜ Task 6.2.1: Create/add missing image assets

**File**: `public/`

**Description**: Ensure all required image assets are in place: skill-issue.jpg (bell curve meme), cortex-stats.png (optional - Cortex report screenshot), skill-tree.png (Ford's skill directory screenshot). Create placeholders or source actual images.

**Depends On**: Tasks 6.1.1

**Actions**:
- ⬜ **6.2.1.1**: CHECK if public/skill-issue.jpg exists, CREATE placeholder if not (`public/skill-issue.jpg`)
- ⬜ **6.2.1.2**: CHECK if public/skill-tree.png exists, CREATE placeholder if not (`public/skill-tree.png`)
- ⬜ **6.2.1.3**: VERIFY all image references in slides point to correct paths

### ⬜ Task Group 6.3: Speaker Notes Pass

**Objective**: Ensure all slides have helpful speaker notes

#### ⬜ Task 6.3.1: Review and complete speaker notes

**File**: `slides/`

**Description**: Review all slides and ensure each has helpful speaker notes. Notes should include: key talking points, timing hints, transition cues.

**Context to Load**:
- `agents/sessions/2025-01-07_agent-skills-presentation_k8m3x9/spec.md` (lines 153-156) - Get time constraints (15 min content, 20 min total)

**Depends On**: Tasks 6.2.1

**Actions**:
- ⬜ **6.3.1.1**: REVIEW all slides for speaker notes completeness (`slides/`)
- ⬜ **6.3.1.2**: ADD timing hints: ~15 min content, skills section 5-7 min (`slides/`)
- ⬜ **6.3.1.3**: ADD transition cues between sections (`slides/`)

### ⬜ Task Group 6.4: Final Build & Run-through

**Objective**: Full presentation verification

#### ⬜ Task 6.4.1: Final build and full run-through

**File**: `None`

**Description**: Final build of slides, complete run-through of presentation, verify all images load, check timing is ~15 min, ensure narrative flow is complete.

**Depends On**: Tasks 6.3.1

**Actions**:
- ⬜ **6.4.1.1**: RUN npm run build:slides for final index.md generation
- ⬜ **6.4.1.2**: RUN npm run dev for final presentation preview
- ⬜ **6.4.1.3**: VERIFY all images load correctly
- ⬜ **6.4.1.4**: VERIFY slide count and estimate ~15 min of content
- ⬜ **6.4.1.5**: VERIFY complete narrative arc: Title -> Problem -> Hook -> Question -> Mental Model -> Skills Concept -> How Skills Work -> Example -> Occam's Razor -> Vision -> Takeaways -> Conclusion

---

---
*Auto-generated from plan.json on 2026-01-07 13:55*