# Agent Skills Presentation Brainstorm

> **Session**: `2025-01-07_agent-skills-presentation_k8m3x9`
> **Status**: FINALIZED
> **Created**: 2025-01-07
> **Finalized**: 2025-01-07

## Overview

AI meetup talk on "AI and Agentic coding in 2026" - what Ford is focusing on and how to actually get real value from AI coding tools. This is a **blank slate** presentation being built from scratch.

### Core Thesis (Emerging)

Twitter/social media is full of flashy demos that burn tokens and make impressive-looking changes. But when you step into a **real codebase** - work you get paid for - things break down. The presentation will show:
1. What "real value" actually looks like (Ford's personal stats as proof)
2. Industry data showing the gap between AI adoption and actual outcomes
3. The solution: Skills as a way to encode expertise and get consistent, quality results

## Problem Statement

**The gap between AI coding demos and production reality.**

People see impressive demos on Twitter - massive token burns, huge diffs, rapid prototypes. But:
- In real codebases (paid work, teams, production), these approaches break down
- 90% adoption, but incidents per PR up 23.5%, change failure rate up 30%
- "More code, more slop" - velocity without quality
- Only 45% have formal AI usage policies - no standardization

## Goals

### High-Level Goals

Audience leaves understanding that **AI amplifies whatever you have** - good foundations = amplified strengths, weak foundations = amplified problems. And that skills/structured approaches are how you encode quality.

### Mid-Level Goals

1. Establish credibility through transparency (Ford's real numbers)
2. Ground the discussion in industry data (Cortex 2026 report)
3. Introduce skills as a concrete solution for "getting it right"
4. Walk through a practical example skill

### Detailed Goals

*To be filled in as we discuss specifics...*

## Non-Goals

*What we are explicitly NOT building - prevents scope creep*

- Not a "Claude Code tutorial" - assume some familiarity
- Not comparing AI tools (Copilot vs Cursor vs Claude Code)
- Not covering MCP in depth (skills reference it but focus stays on skills)

## Success Criteria

*How do we know we're done? Testable outcomes*

- [ ] Opening hook lands - audience understands the "real value vs demo" distinction
- [ ] Industry data resonates - they see themselves in the "more code, more bugs" paradox
- [ ] Skills concept clicks - they understand what skills are and why they matter
- [ ] Actionable takeaway - they know HOW to start applying this

## Context & Background

### Presentation Structure (Emerging)

**Opening Hook:**
- Ford's personal stats: diff changes, token spend, money made (past 30 days)
- NOT a flex - it's proof of "real value" vs Twitter demos
- Contrast: You can burn tokens and make changes, but are you creating lines that provide real value?

**Industry Data (Cortex 2026 Benchmark Report):**
- ~90% of engineering leaders report teams actively using AI tools
- "90% adoption, zero standardization"
- The Productivity Paradox:
  - PRs per author +20%
  - Incidents per PR +23.5%
  - Change failure rate +30%
- Key insight: "AI amplifies both the best and worst aspects of your engineering practices"

**The Mental Model - Agent as Junior Engineer:**
- Senior engineer workflow: Create spec/task → hand to junior → review PR → merge
- You don't hand complex tasks to a brand-new junior (they get chores, minor refactoring)
- More complex tasks go to the engineer who's been on the project 7 months
- Goal: Build agents we can hand increasingly complex tasks to
- Skills are HOW you level up the agent's capability

**The Recipe** (crucial for Claude Code & other agents like Codex, OpenCode):
1. Modularity
2. Domain-Driven Design
3. Painfully explicit specs
4. Excessive documentation

If the docs don't clearly answer: **Where, What, How, Why** → agent guesses → mess

**The Solution - Skills:**
- How Ford sets up skills for himself and teams
- What a skill is structurally (how it's represented in the prompt)
- Example skill walkthrough

### From Current Notes

- **Occam's Razor**: "So much of AI is significantly overcomplicated"
- **Loop pattern**: "In loop → iterate until it works well → figure out how to step out of loop"
- **Frontend debugging example**: Screenshot → console logs → add logs → test → user feedback loop
- "Get this working right instead of just letting the agent rip"
- **Separate Concerns**: Research, spec, and plan should be separate (not one mega-prompt)
- References: Wirasm/PRPs-agentic-eng, greyhaven-ai/claude-code-config

### Skills Background (from blog post reference)

Evolution: Function Calling → MCP → Agent Skills
- Skills = "Knowledge & Workflow layer" - procedural expertise
- Progressive disclosure - only load context as necessary
- Best practices: conciseness, appropriate degrees of freedom, frontload info

## Key Decisions

*Capture the WHY behind decisions, not just the WHAT. Include user's reasoning and preferences.*

| Decision | Rationale | Date |
|----------|-----------|------|
| Start with personal stats | Credibility through transparency, not bragging - shows "this is what real value looks like" | 2025-01-07 |
| Use Cortex report data | Third-party validation of the "more code, more bugs" problem | 2025-01-07 |
| Frame as "you already do this with humans" | Demystifies agents - it's not new, it's the same standardization you do with junior engineers, just formatted for an LLM | 2025-01-07 |
| Include the "recipe" (Modularity, DDD, explicit specs, docs) | This is the "how" that bridges problem to solution - without these, agent guesses and makes a mess | 2025-01-07 |
| Include personal anecdote of bad AI usage | Grounds "AI amplifies whatever you have" in real experience - the client project with 5000-line files | 2025-01-07 |
| End with "don't let bad examples blind you" | Crucial reframe - yes the horror stories are real, but for skilled engineers this is a massive opportunity | 2025-01-07 |
| Push back on "10x engineer" myth | Set realistic expectations - it's 10% here, 5% there, compounding over months. No magic pill. | 2025-01-07 |
| Include concrete ROI math ($10K → $40K value) | Makes the value prop undeniable - spend $10K in tokens to get $40K in engineering value. No-brainer. | 2025-01-07 |

## Open Questions

- [x] What specific aspects of agent skills should the presentation focus on? → Structure, example skill, "how Ford sets up his own"
- [x] Who is the target audience for this presentation? → AI meetup attendees (likely devs/engineers interested in AI coding)
- [ ] What specific example skill do you want to walk through? → TBD (pin for now)
- [x] What are your actual numbers for the opening? → +114,427 lines, ~$864 tokens, $23,480 income
- [x] How technical should the skill walkthrough be? → Light touch, 5-7 min, not deep in the weeds
- [x] What's the "one thing" you want them to remember/do after leaving? → See below

### The One Takeaway

We're stepping out of the conceptual idea that "AI won't actually be coming for us" or "using AI doesn't actually yield results."

**The reality:**
- AI is becoming truly useful for development tasks BEYOND just MVP projects
- It can work with real infrastructure IF you put effort into teaching it AND you know what you're doing
- It doesn't REPLACE your skills - it gives skilled engineers more LEVERAGE
- It does NOT replace the knowledge you've accrued

### Time Constraints

- ~20 min presentation (including Q&A)
- Aiming for ~15 min of content
- Skills section: 5-7 min (light touch, not deep weeds)

## Presentation Outline

```
The Skill Issue
├── 00-title/
│   ├── "The Skill Issue"
│   ├── Subtitle: "Agents Decoded in 2026"
│   └── QR code for follow-along
│
├── 01-the-problem/
│   ├── Industry data: 90% adoption, zero standardization (Cortex 2026)
│   │   └── Link to Cortex report, show key images/stats
│   ├── The Productivity Paradox:
│   │   ├── PRs per author +20%
│   │   ├── Incidents per PR +23.5%
│   │   └── Change failure rate +30%
│   ├── "AI amplifies whatever you have" - I've seen this firsthand:
│   │   ├── Recent client project - had to refactor thousands of lines
│   │   ├── UI engineer using Cursor without understanding
│   │   ├── Hardcoded strings, 5000+ line files, 20 components per file
│   │   └── Not his fault - he didn't know what he was doing
│   ├── Everyone has seen this: bad engineer + AI = shitstorm to clean up
│   ├── THE MEME (skill-issue.jpg) - the bell curve:
│   │   ├── Left: "Let AI Write the Code"
│   │   ├── Middle (crying): "AI Cannot Match my Skills"
│   │   └── Right (enlightened): "Let AI Write the Code"
│   └── BUT: Don't let bad examples blind you to the opportunity
│       └── For skilled engineers, AI is a HUGE force multiplier
│
├── 02-about-me-and-hook/
│   ├── Who am I: Ford Lascari - Applied AI Engineer, 3 years GenAI, ~2 years agentic
│   ├── Why should you trust me? (the hook)
│   ├── Screenshots revealed on each click:
│   │   ├── Click 1: Line count (+114,427 lines added)
│   │   ├── Click 2: Token spend (~$864 in Claude Code)
│   │   └── Click 3: Income ($23,480 December)
│   ├── KICKER: "95% of the code was written by AI"
│   └── This isn't a flex - it's proof that real value IS possible
│
├── 03-the-question/
│   ├── Now that we've defined the problem...
│   ├── What are we doing in 2026 to fix this?
│   ├── What should you allocate your time and resources to?
│   └── How do you build TRUST into your AI system?
│
├── 04-the-mental-model/
│   ├── "This isn't new - every engineering team already does this"
│   ├── When you work with a junior engineer:
│   │   ├── You determine what the task should be
│   │   ├── You hand it off
│   │   ├── You review the PR
│   │   └── HOW it gets done? You don't control that
│   ├── But there's implicit/explicit STANDARDIZATION that keeps things in line:
│   │   ├── Commit rules
│   │   ├── Tests must pass
│   │   ├── GitHub Actions
│   │   ├── Company protocols
│   │   └── Documentation the junior reads to understand YOUR standards
│   └── The goal: Transition that standardization into something the LLM can act upon
│       └── Same docs you'd give a new junior = what you give the LLM
│
├── 05-what-is-a-skill/
│   ├── Skills = opinionated way of formatting Markdown files
│   ├── Allows agent to SELF-DISCOVER processes within the skill
│   ├── Anthropic recently released this, becoming the standard structure
│   └── Not that complicated to set up
│
├── 06-how-skills-work/
│   ├── Top-level structure (show from Anthropic blog/images)
│   ├── How it appears in the prompt:
│   │   ├── Model sees: "I have these skills available"
│   │   ├── Model thinks: "I need to acquire this skill"
│   │   ├── Model reads the skill files
│   │   └── Now that knowledge is IN the context window
│   ├── File tree structure:
│   │   ├── SKILL.md (main file)
│   │   ├── references/ (linked docs)
│   │   └── "For this workflow, go to this file"
│   └── Progressive disclosure - only load context when needed
│
├── 07-the-vision/
│   ├── What we're doing with skills = encoding your engineering knowledge
│   ├── First: Agent efficiently does flows you already do
│   ├── Then: Trust builds → queue as background task → just review
│   ├── Goal: Step farther and farther out of the loop
│   ├── REALITY CHECK - Pushback on "10x engineer" myth:
│   │   ├── 10x output is NOT instant transformation
│   │   ├── Reality: 10% faster here, 5% faster there
│   │   ├── These compound over MONTHS
│   │   ├── No magic pill - AI does NOT replace knowledge
│   │   └── You're building TOWARDS that future, not there yet
│   └── Don't "just let AI handle it completely" - but build toward it
│
├── 08-example-skill/
│   ├── Show file tree of Ford's Claude Code config
│   │   └── "I have a lot of skills/commands built out"
│   ├── "This isn't comprehensive - this is how I work"
│   ├── Focus on ONE specific skill [TBD which one]
│   ├── OCCAM'S RAZOR approach to building skills:
│   │   ├── Common mistake: give everything to the agent right out the gate
│   │   ├── This leads to bad skills - flow isn't tested, not based on YOUR flow
│   │   ├── Right approach: Work IN the loop first
│   │   ├── Iterate until you're happy with how it works
│   │   ├── THEN: "How can I take myself out of it?"
│   │   └── Keep it as simple as possible - don't add complexity until you need it
│   ├── Show how I go about making them
│   └── How this standardizes a process you + agent can leverage
│   └── (Light touch, 5-7 min total for skills section)
│
├── 09-key-takeaways/
│   ├── Don't let bad examples blind you - this is coming
│   ├── For skilled engineers, AI is a HUGE force multiplier
│   ├── The Math (makes it a no-brainer):
│   │   ├── Each engineer using ~$1,000/month in tokens (like me)
│   │   ├── 10 engineers = $10,000/month token spend
│   │   ├── Average engineer costs ~$10,000/month
│   │   ├── 40% more effective = value of 4 extra engineers = $40,000/month
│   │   ├── Spend $10K to get $40K value = 4x ROI
│   │   └── The hard part: getting there, knowing what to invest time in
│   ├── The Mentality:
│   │   ├── What can we systematize into skills?
│   │   └── Transfer best practices from top performers to whole team
│   └── Skills = encoding your engineering knowledge → compound gains over time
│
└── 10-conclusion/
    ├── Let's Connect - QR codes (X, LinkedIn, Website)
    └── Questions?
```

## Diagrams

*Mermaid or ASCII diagrams as understanding develops*

## Notes

*Working notes, ideas, considerations*

- The "Occam's Razor" framing is powerful - overcomplicated AI setups are the enemy
- The loop pattern (iterate until it works, then step out) feels like a key insight
- "Separate Concerns" could be a structural principle for the skills section
- The agent-session skill in this very repo could be a meta-example

---
*Spec finalized on 2025-01-07. Ready for `/plan` phase.*
