---
theme: ../
layout: default
clicks: 2
---

<div class="text-center">
<h1>What Skills Do I Need?</h1>
</div>

<!-- Container for all steps - same position -->
<div class="relative min-h-96">

<!-- Scene 1: Everyone has different workflows -->
<div v-if="$clicks >= 1 && $clicks < 2" class="absolute inset-0">
<div class="bg-white border-blue-600 border-1 rounded-lg p-6">
<h3 class="text-xl font-bold text-blue-600 mb-4">Everyone Has Different Workflows</h3>
<div class="grid grid-cols-4 gap-4">
<div class="bg-gray-50 border border-gray-200 rounded-lg p-4 text-center">
<div class="text-3xl mb-2">🔧</div>
<div class="font-bold text-gray-900">Backend Dev</div>
<div class="text-xs text-gray-500 mt-2">API design, DB migrations, testing patterns</div>
</div>
<div class="bg-gray-50 border border-gray-200 rounded-lg p-4 text-center">
<div class="text-3xl mb-2">🎨</div>
<div class="font-bold text-gray-900">Frontend Dev</div>
<div class="text-xs text-gray-500 mt-2">Component patterns, debugging, styling</div>
</div>
<div class="bg-gray-50 border border-gray-200 rounded-lg p-4 text-center">
<div class="text-3xl mb-2">📊</div>
<div class="font-bold text-gray-900">Data Engineer</div>
<div class="text-xs text-gray-500 mt-2">Pipeline workflows, SQL patterns, ETL</div>
</div>
<div class="bg-gray-50 border border-gray-200 rounded-lg p-4 text-center">
<div class="text-3xl mb-2">🚀</div>
<div class="font-bold text-gray-900">DevOps</div>
<div class="text-xs text-gray-500 mt-2">CI/CD, infra-as-code, monitoring</div>
</div>
</div>
<div class="mt-4 border-t border-gray-300 pt-4 text-center text-black font-medium flex justify-center gap-6">
<span>Different Roles.</span>
<span>Different Problems.</span>
<span>Different Skills.</span>
</div>
</div>
</div>

<!-- Scene 2: My setup + "what do I even show?" -->
<div v-if="$clicks >= 2" class="absolute inset-0">
<div class="bg-white border-amber-600 border-1 rounded-lg p-6">
<h3 class="text-xl font-bold text-amber-600 mb-4">I Have a Lot of Skills...</h3>
<div class="grid grid-cols-3 gap-6">
<div class="col-span-2 bg-gray-50 border border-gray-200 rounded-lg p-4 font-mono text-xs">
<div class="text-gray-500 mb-2"># My actual .claude/ directory</div>
<div class="text-gray-900">.claude/</div>
<div class="ml-4 text-gray-600">├── agents/ <span class="text-gray-400">(7 files)</span></div>
<div class="ml-4 text-gray-600">├── commands/ <span class="text-gray-400">(28 files)</span></div>
<div class="ml-4 text-gray-600">├── hooks/ <span class="text-gray-400">(3 files)</span></div>
<div class="ml-4 text-blue-600 font-bold">└── skills/ <span class="text-gray-400">(98 files)</span></div>
<div class="ml-8 text-blue-500">├── agent-session/ (21)</div>
<div class="ml-8 text-blue-500">├── browser-mcp/ (5)</div>
<div class="ml-8 text-blue-500">├── docs-framework/ (52)</div>
<div class="ml-8 text-blue-500">├── git/ (2)</div>
<div class="ml-8 text-blue-500">├── prompt-writing/ (10)</div>
<div class="ml-8 text-blue-500">└── skill-creator/ (8)</div>
<div class="mt-3 text-green-600 font-bold">Total: 141 files</div>
</div>
<div class="col-span-1">
<div class="bg-amber-50 border-2 border-amber-600 rounded-lg p-4">
<div class="text-amber-600 font-bold mb-2">But What Do I Show You?</div>
<div class="text-sm text-gray-700">My workflow is probably not the same as yours.</div>
<div class="text-sm text-gray-900 font-medium mt-3">Everyone is different.</div>
</div>
</div>
</div>
</div>
</div>

</div>

<!--
This slide addresses "what skills do I need?" - the answer is: it depends. Everyone has different workflows. I show my 141-file setup, but acknowledge that my workflow isn't yours.
-->
