---
theme: ../
layout: default
---

# The Problem

<div class="mt-8 space-y-6">

<div class="text-2xl font-bold text-center mb-8">
90% AI adoption, zero standardization
</div>

<div class="grid grid-cols-3 gap-6 text-center">
  <div class="p-4 bg-red-500/10 rounded-lg">
    <div class="text-3xl font-bold text-red-400">+20%</div>
    <div class="text-sm text-gray-400">PRs per author</div>
  </div>
  <div class="p-4 bg-orange-500/10 rounded-lg">
    <div class="text-3xl font-bold text-orange-400">+23.5%</div>
    <div class="text-sm text-gray-400">Incidents per PR</div>
  </div>
  <div class="p-4 bg-red-600/10 rounded-lg">
    <div class="text-3xl font-bold text-red-500">+30%</div>
    <div class="text-sm text-gray-400">Change failure rate</div>
  </div>
</div>

<v-click>
<div class="text-xl text-center mt-8 italic text-gray-300">
"AI amplifies whatever you have"
</div>
</v-click>

<v-click>
<div class="mt-6 p-4 bg-slate-800/50 rounded-lg border-l-4 border-orange-400">
<div class="text-lg font-semibold mb-2">I've seen this firsthand:</div>
<div class="text-sm text-gray-300 space-y-1">
  <div>Recent client project - UI engineer using Cursor without understanding</div>
  <div>5000+ line files, hardcoded strings, 20 components per file</div>
  <div class="italic text-gray-400 mt-2">Not his fault - he didn't know what he was doing</div>
</div>
</div>
</v-click>

</div>

<!--
This data is from the Cortex 2026 State of Engineering report. 90% of developers are now using AI tools - but look at what's happening to quality metrics. More code is shipping, but incidents are up, failure rates are up. The pattern is clear: AI amplifies whatever you already have. Good practices become great. Bad practices become catastrophic.

Personal anecdote: I had to refactor thousands of lines from this client. The engineer wasn't bad - he just didn't have the experience to guide the AI properly. This is the skill issue - not the AI's fault, not the engineer's fault necessarily, but a gap in knowing HOW to work with AI effectively.
-->

<style>
  .text-slate-steel { color: #4C5A61; }
  .text-bone-white { color: #EAE7DC; }
</style>
