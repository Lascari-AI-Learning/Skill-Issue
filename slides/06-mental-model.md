---
theme: ../
layout: default
---

# Before We Get Into the "How"...

<div class="text-lg text-gray-600 mb-6">Let's make this concrete. Think about working with a junior engineer.</div>

<div class="grid grid-cols-2 gap-8">

<div v-click class="bg-white border-blue-600 border-1 rounded-lg p-5">
<h3 class="text-xl font-bold text-blue-600 mb-4">The Handoff</h3>
<div class="space-y-3">
<div class="flex items-start gap-2">
  <span class="text-blue-600 font-bold">1.</span>
  <span>You scope out the task</span>
</div>
<div class="flex items-start gap-2">
  <span class="text-blue-600 font-bold">2.</span>
  <span>You hand it off</span>
</div>
<div class="flex items-start gap-2">
  <span class="text-blue-600 font-bold">3.</span>
  <span>They implement <span class="text-gray-400 italic text-sm">(you're not watching)</span></span>
</div>
<div class="flex items-start gap-2">
  <span class="text-blue-600 font-bold">4.</span>
  <span>You review the PR, give feedback</span>
</div>
</div>
</div>

<div v-click class="bg-white border-emerald-600 border-1 rounded-lg p-5">
<h3 class="text-xl font-bold text-emerald-600 mb-4">But You Don't Just Wing It</h3>
<div class="space-y-2 text-lg">
<div class="flex items-center gap-2">
  <span class="text-emerald-600">→</span>
  <span>Tests that must pass</span>
</div>
<div class="flex items-center gap-2">
  <span class="text-emerald-600">→</span>
  <span>Commit rules & linting</span>
</div>
<div class="flex items-center gap-2">
  <span class="text-emerald-600">→</span>
  <span>GitHub Actions / CI</span>
</div>
<div class="flex items-center gap-2">
  <span class="text-emerald-600">→</span>
  <span>Company protocols</span>
</div>
<div class="flex items-center gap-2">
  <span class="text-emerald-600">→</span>
  <span>Documentation to read first</span>
</div>
</div>
</div>

</div>

<v-click>
<div class="mt-6 bg-white border-amber-600 border-1 rounded-lg p-4 text-center text-xl">
<div class="text-gray-700">Working with AI is the same.</div>
<div class="font-bold text-amber-600">Encode this information so the AI can operate at scale.</div>
</div>
</v-click>

<!--
Before we get into the actual techniques - let's make this concrete. Handing something off to a computer can feel jarring. So think about it like working with a junior engineer you just brought onto the team.

If you just say "here's a ticket: update this service" and expect magic - what's going to happen? That PR is probably not going to be amazing.

But in an organization, there's standardization. The flow is: scope the task, hand it off, they implement (you don't watch over their shoulder), you review the PR and give feedback. You don't control HOW they write each line.

BUT you don't just wing it either. You have tests, commit rules, CI/CD, company protocols, documentation they read before touching core code.

Working with AI is similar - you need to figure out how to encode this same information so the AI can operate at scale across a wide variety of tasks. The end goal: give it a scoped task, it goes off and does it, you review the PR and make a few changes.
-->
