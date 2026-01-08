---
theme: ../
layout: default
clicks: 6
---

<div class="flex justify-center items-start">
<h1>Example: Front-End Debug Skill</h1>
</div>

<!-- Container for all steps - same position -->
<div class="relative min-h-96">

<!-- Scene 1: The problem this skill solves -->
<div v-if="$clicks >= 1 && $clicks < 3" class="absolute inset-0">
<div class="bg-white border-blue-600 border-1 rounded-lg p-6">
<h3 class="text-xl font-bold text-blue-600 mb-4">The Problem</h3>
<div class="grid grid-cols-2 gap-6">
<div class="bg-gray-50 border border-gray-300 rounded-lg p-4">
<div class="text-gray-800 font-medium mb-3">The Manual Debugging Loop:</div>
<ol class="space-y-2 text-sm text-gray-700 list-decimal list-inside">
<li>Add console.log statements</li>
<li>Reload the page</li>
<li>Screenshot the page</li>
<li>Copy console output</li>
<li>Paste into AI chat</li>
<li>Discuss, repeat...</li>
</ol>
</div>
<div v-click="2" class="bg-blue-50 border-2 border-blue-600 rounded-lg p-4">
<div class="text-blue-600 font-bold mb-3">What If the Agent Could:</div>
<ul class="space-y-2 text-sm text-gray-900">
<li>Add debug logs itself</li>
<li>Refresh the page for you</li>
<li>Pull console logs directly</li>
<li>Screenshot the page automatically</li>
<li>Clean up when done completely</li>
</ul>
</div>
</div>
</div>
</div>

<!-- Scene 2: The SKILL.md + Workflow -->
<div v-if="$clicks >= 3 && $clicks < 4" class="absolute inset-0">
<div class="bg-white border-green-600 border-1 rounded-lg p-6">
<div class="flex justify-between mb-4">
<h3 class="text-xl font-bold text-green-600">The Skill</h3>
<h3 class="text-xl font-bold text-green-600">The Workflow</h3>
</div>
<div class="grid grid-cols-2 gap-4">
<div class="bg-gray-50 border border-gray-300 rounded-lg p-3 font-mono text-xs">
<div class="text-gray-500 text-xs mb-2"># SKILL.md</div>
<div class="text-amber-600">---</div>
<div><span class="text-blue-600">name:</span> browser-mcp</div>
<div><span class="text-blue-600">description:</span> Browser automation</div>
<div class="text-amber-600">---</div>
<div class="mt-2 text-green-600 font-bold"># Tools</div>
<div class="text-gray-700">browser_screenshot, browser_navigate</div>
<div class="text-gray-700">browser_get_console_logs, ...</div>
<div class="mt-2 text-green-600 font-bold"># Debug Log Convention</div>
<div class="text-gray-700">console.log(<span class="text-amber-600">'[DEBUG-AGENT]'</span>,</div>
<div class="text-gray-700 ml-2"><span class="text-amber-600">'[Context]'</span>, { data });</div>
<div class="mt-2 text-green-600 font-bold"># Cookbook</div>
<div class="text-gray-700">- IF: Debugging front-end</div>
<div class="text-gray-700 ml-2">THEN: workflows/debug.md</div>
</div>
<div class="bg-gray-50 border border-gray-300 rounded-lg p-3 font-mono text-xs">
<div class="text-gray-500 text-xs mb-2"># workflows/debug.md</div>
<div class="text-purple-600">&lt;workflow id="frontend-debugging"&gt;</div>
<div class="ml-2 text-blue-600">&lt;phase name="Setup"&gt;</div>
<div class="ml-4 text-gray-600">Confirm page with user...</div>
<div class="ml-2 text-amber-600">&lt;loop name="Debug"&gt;</div>
<div class="ml-4 text-teal-600">&lt;step name="Observe"&gt;</div>
<div class="ml-6 text-gray-600">Screenshot + console logs...</div>
<div class="ml-4 text-teal-600">&lt;step name="Instrument"&gt;</div>
<div class="ml-6 text-gray-600">Add [DEBUG-AGENT] logs...</div>
<div class="ml-4 text-teal-600">&lt;step name="Refresh"&gt;</div>
<div class="ml-6 text-gray-600">Reload, re-observe...</div>
<div class="ml-2 text-amber-600">&lt;/loop&gt;</div>
<div class="ml-2 text-blue-600">&lt;phase name="Fix"&gt;</div>
<div class="ml-4 text-gray-600">Apply solution...</div>
<div class="ml-2 text-blue-600">&lt;phase name="Cleanup"&gt;</div>
<div class="ml-4 text-gray-600">Remove all markers...</div>
<div class="text-purple-600">&lt;/workflow&gt;</div>
</div>
</div>
</div>
</div>

<!-- Scene 3: The workflow -->
<div v-if="$clicks >= 4" class="absolute inset-0">
<!-- Workflow diagram in orange box -->
<div class="bg-white border-amber-600 border-1 rounded-lg p-6">
<div class="flex items-center gap-3">
<!-- Setup -->
<div class="bg-blue-100 border-2 border-blue-400 rounded px-4 py-3 text-center">
<div class="text-sm text-blue-700 font-bold">SETUP</div>
<div class="text-xs text-gray-600">Confirm page</div>
</div>
<div class="text-gray-400 text-xl">→</div>
<!-- Debug Loop -->
<div class="border-2 border-dashed border-amber-400 rounded-lg p-3 bg-amber-50">
<div class="text-xs text-amber-600 font-bold text-center mb-2">DEBUG LOOP</div>
<div class="flex items-center gap-2">
<div class="bg-green-100 border border-green-300 rounded px-3 py-2 text-center">
<div class="text-xs text-green-700 font-bold">OBSERVE</div>
<div class="text-xs text-gray-600">Screenshot + logs</div>
</div>
<div class="text-gray-400">→</div>
<div class="bg-amber-100 border border-amber-300 rounded px-3 py-2 text-center">
<div class="text-xs text-amber-700 font-bold">INSTRUMENT</div>
<div class="text-xs text-gray-600">Add debug logs</div>
</div>
<div class="text-gray-400">→</div>
<div class="bg-purple-100 border border-purple-300 rounded px-3 py-2 text-center">
<div class="text-xs text-purple-700 font-bold">REFRESH</div>
<div class="text-xs text-gray-600">Reload page</div>
</div>
</div>
</div>
<div class="text-gray-400 text-xl">→</div>
<!-- Fix -->
<div class="bg-green-100 border-2 border-green-400 rounded px-4 py-3 text-center">
<div class="text-sm text-green-700 font-bold">FIX</div>
<div class="text-xs text-gray-600">Apply solution</div>
</div>
<div class="text-gray-400 text-xl">→</div>
<!-- Cleanup -->
<div class="bg-red-100 border-2 border-red-400 rounded px-4 py-3 text-center">
<div class="text-sm text-red-700 font-bold">CLEANUP</div>
<div class="text-xs text-gray-600">Remove markers</div>
</div>
</div>
</div>
<!-- Progressive reveal boxes outside the workflow div -->
<div class="grid grid-cols-2 gap-4 mt-4">
<div v-click="5" class="bg-gray-50 border-2 border-gray-400 rounded-lg p-4">
<div class="text-gray-800 font-bold mb-2">Agent Handles Mechanical Tedium</div>
<ul class="text-sm text-gray-700 space-y-1">
<li>Taking screenshots of the page</li>
<li>Pulling console logs</li>
<li>Adding instrumentation</li>
<li>Refreshing and re-capturing</li>
</ul>
</div>
<div v-click="6" class="bg-blue-50 border-2 border-blue-400 rounded-lg p-4">
<div class="text-blue-700 font-bold mb-2">User Confirms Judgment Calls</div>
<ul class="text-sm text-gray-700 space-y-1">
<li>"Is this the right page?"</li>
<li>"I'm seeing something different..."</li>
<li>"Does this fix seem right?"</li>
<li>"Based on the codebase, should we..."</li>
</ul>
</div>
</div>
</div>

</div>

<!--
This slide shows a real example: the browser-mcp skill for front-end debugging.

The problem: Debugging React/Next.js state issues involves a tedious manual loop of adding console.logs, reloading, screenshotting, and pasting into AI chat.

The skill: Uses Browser MCP to automate this. Agent can add debug logs (with [DEBUG-AGENT] marker for easy cleanup), refresh the page, capture console logs and screenshots directly.

The workflow: Setup → Observe → Instrument → Refresh → Iterate → Fix → Cleanup

Key insight: Agent handles mechanical tedium, user stays in loop for judgment calls. The log convention ensures clean removal when done.
-->
