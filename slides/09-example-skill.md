---
theme: ../
layout: default
---

# Example: My Skills Setup

<div class="grid grid-cols-2 gap-8 mt-6">

<div>
<div class="text-gray-300 mb-4">This is how <span class="font-bold text-iron-ochre">I</span> work - not comprehensive, but practical.</div>

<div v-click class="bg-ash-graphite rounded-lg p-4">
<div class="font-mono text-sm">
<div class="text-gray-300">.claude/</div>
<div class="ml-4 text-gray-400">settings.json</div>
<div class="ml-4 text-blue-400">skills/</div>
<div class="ml-8 text-green-400">agent-session/</div>
<div class="ml-8 text-green-400">commit/</div>
<div class="ml-8 text-green-400">pr-review/</div>
<div class="ml-8 text-green-400">prime/</div>
<div class="ml-8 text-gray-400">...</div>
</div>
</div>

<div v-click class="mt-4 text-sm text-gray-400 italic">
I have a lot of skills/commands built out - each one codifies a workflow I do repeatedly.
</div>
</div>

<div v-click>
<h3 class="text-xl font-bold text-iron-ochre mb-4">What's in a Skill?</h3>
<div class="space-y-3">
<div class="p-3 bg-ash-graphite rounded-lg">
  <div class="font-bold text-blue-400">SKILL.md</div>
  <div class="text-sm text-gray-300">Entry point - describes what the skill does and when to use it</div>
</div>
<div class="p-3 bg-ash-graphite rounded-lg">
  <div class="font-bold text-blue-400">Workflows</div>
  <div class="text-sm text-gray-300">Step-by-step processes the agent follows</div>
</div>
<div class="p-3 bg-ash-graphite rounded-lg">
  <div class="font-bold text-blue-400">References</div>
  <div class="text-sm text-gray-300">Examples, templates, domain knowledge</div>
</div>
</div>
</div>

</div>

<div v-click class="mt-6 p-4 bg-ash-graphite rounded-lg text-center">
<span class="text-xl">This standardizes a process <span class="text-iron-ochre">you + agent</span> can leverage</span>
</div>

<!--
Here's what my actual Claude Code config looks like. I have skills for different workflows - agent sessions for planning, commit for standardized commits, PR review, priming context, and more. Each skill encodes a workflow I do repeatedly.

A skill typically has a SKILL.md as the entry point, workflow definitions that the agent follows step-by-step, and references for examples and domain knowledge. The key insight: this standardizes a process that BOTH you and the agent can use. You know exactly what the agent will do because you defined it.

Light touch here - we're spending 5-7 minutes total on the skills section. The goal is understanding, not comprehensive coverage.
-->
