---
theme: ../
layout: default
---

# This Isn't New

<div class="grid grid-cols-2 gap-8 mt-8">

<div>
<h3 class="text-xl font-bold text-blue-400 mb-4">Working with a Junior Engineer</h3>
<div class="space-y-3">
<div v-click class="flex items-start gap-2">
  <span class="text-green-400">1.</span>
  <span>You determine what the task should be</span>
</div>
<div v-click class="flex items-start gap-2">
  <span class="text-green-400">2.</span>
  <span>You hand it off</span>
</div>
<div v-click class="flex items-start gap-2">
  <span class="text-green-400">3.</span>
  <span>You review the PR</span>
</div>
<div v-click class="flex items-start gap-2 text-gray-400 italic">
  <span class="text-yellow-400">?</span>
  <span>HOW it gets done? You don't control that</span>
</div>
</div>
</div>

<div v-click>
<h3 class="text-xl font-bold text-iron-ochre mb-4">But There's Standardization</h3>
<div class="space-y-2 text-lg">
<div class="flex items-center gap-2">
  <span class="text-gray-400">-</span>
  <span>Commit rules</span>
</div>
<div class="flex items-center gap-2">
  <span class="text-gray-400">-</span>
  <span>Tests must pass</span>
</div>
<div class="flex items-center gap-2">
  <span class="text-gray-400">-</span>
  <span>GitHub Actions</span>
</div>
<div class="flex items-center gap-2">
  <span class="text-gray-400">-</span>
  <span>Company protocols</span>
</div>
<div class="flex items-center gap-2">
  <span class="text-gray-400">-</span>
  <span>Documentation</span>
</div>
</div>
</div>

</div>

<div v-click class="mt-8 p-4 bg-ash-graphite rounded-lg text-center text-xl">
<span class="text-gray-300">The same docs you'd give a new junior</span> = <span class="font-bold text-blue-400">what you give the LLM</span>
</div>

<!--
This isn't a new concept - every engineering team already does this. When you onboard a junior engineer, you don't control HOW they write code line by line. You give them the task, the context, the standards, and you review the output. The key is implicit and explicit standardization - commit rules, tests, CI/CD, documentation. The goal with skills is to transition that standardization into something the LLM can act upon. The same docs you'd hand a new hire? That's what you encode for the AI.
-->
