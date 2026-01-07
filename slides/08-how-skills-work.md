---
theme: ../
layout: default
---

# How Skills Work

<div class="grid grid-cols-2 gap-8 mt-6">

<div>
<h3 class="text-xl font-bold text-blue-400 mb-4">The Flow</h3>
<div class="space-y-3">
<div v-click class="flex items-start gap-3 p-3 bg-ash-graphite rounded-lg">
  <span class="text-2xl">1.</span>
  <div>
    <span class="text-gray-300">Model sees:</span>
    <span class="font-bold text-iron-ochre">"I have these skills available"</span>
  </div>
</div>
<div v-click class="flex items-start gap-3 p-3 bg-ash-graphite rounded-lg">
  <span class="text-2xl">2.</span>
  <div>
    <span class="text-gray-300">Model thinks:</span>
    <span class="font-bold text-iron-ochre">"I need to acquire this skill"</span>
  </div>
</div>
<div v-click class="flex items-start gap-3 p-3 bg-ash-graphite rounded-lg">
  <span class="text-2xl">3.</span>
  <span>Model reads the skill files</span>
</div>
<div v-click class="flex items-start gap-3 p-3 bg-ash-graphite rounded-lg">
  <span class="text-2xl">4.</span>
  <span class="font-bold text-green-400">Knowledge is now IN the context</span>
</div>
</div>
</div>

<div v-click>
<h3 class="text-xl font-bold text-iron-ochre mb-4">File Structure</h3>
<div class="font-mono text-sm bg-ash-graphite p-4 rounded-lg">
<div class="text-gray-300">.claude/skills/</div>
<div class="ml-4 text-blue-400">my-skill/</div>
<div class="ml-8 text-green-400">SKILL.md</div>
<div class="ml-8 text-gray-400">references/</div>
<div class="ml-12 text-gray-400">workflow.md</div>
<div class="ml-12 text-gray-400">examples.md</div>
</div>
</div>

</div>

<div v-click class="mt-6 p-4 bg-ash-graphite rounded-lg border-l-4 border-blue-400">
<div class="font-bold text-xl">Progressive Disclosure</div>
<div class="text-gray-300 mt-1">Only load context when needed - keeps the context window lean</div>
</div>

<!--
Here's the magic of how skills work. The model sees a list of available skills in the system prompt. When it needs to do something, it thinks "I should acquire this skill" and reads the skill files. Now that knowledge is IN the context window - the agent has your engineering knowledge on demand.

The file structure is simple: SKILL.md is the main entry point, and references/ contains linked documentation for different workflows. This enables progressive disclosure - the agent only loads what it needs, when it needs it.
-->
