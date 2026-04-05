<template>
  <div class="space-y-8">

    <!-- Colors -->
    <div>
      <h3 class="text-zinc-400 text-sm font-semibold uppercase tracking-widest mb-4">Colors</h3>
      <div class="flex flex-wrap gap-3">
        <span class="px-3 py-1 rounded-full text-xs font-bold bg-pink-500/20 text-pink-400 border border-pink-500/30">Pink</span>
        <span class="px-3 py-1 rounded-full text-xs font-bold bg-violet-500/20 text-violet-400 border border-violet-500/30">Violet</span>
        <span class="px-3 py-1 rounded-full text-xs font-bold bg-emerald-500/20 text-emerald-400 border border-emerald-500/30">Green</span>
        <span class="px-3 py-1 rounded-full text-xs font-bold bg-amber-500/20 text-amber-400 border border-amber-500/30">Amber</span>
        <span class="px-3 py-1 rounded-full text-xs font-bold bg-red-500/20 text-red-400 border border-red-500/30">Red</span>
        <span class="px-3 py-1 rounded-full text-xs font-bold bg-sky-500/20 text-sky-400 border border-sky-500/30">Sky</span>
      </div>
    </div>

    <!-- Status -->
    <div>
      <h3 class="text-zinc-400 text-sm font-semibold uppercase tracking-widest mb-4">Status</h3>
      <div class="flex flex-wrap gap-3">
        <span class="px-3 py-1 rounded-full text-xs font-bold bg-emerald-500/20 text-emerald-400 border border-emerald-500/30 flex items-center gap-1.5">
          <span class="w-1.5 h-1.5 rounded-full bg-emerald-400 animate-pulse"></span>
          Active
        </span>
        <span class="px-3 py-1 rounded-full text-xs font-bold bg-amber-500/20 text-amber-400 border border-amber-500/30 flex items-center gap-1.5">
          <span class="w-1.5 h-1.5 rounded-full bg-amber-400"></span>
          Pending
        </span>
        <span class="px-3 py-1 rounded-full text-xs font-bold bg-red-500/20 text-red-400 border border-red-500/30 flex items-center gap-1.5">
          <span class="w-1.5 h-1.5 rounded-full bg-red-400"></span>
          Offline
        </span>
        <span class="px-3 py-1 rounded-full text-xs font-bold bg-zinc-700/50 text-zinc-400 border border-zinc-700 flex items-center gap-1.5">
          <span class="w-1.5 h-1.5 rounded-full bg-zinc-400"></span>
          Archived
        </span>
      </div>
    </div>

    <!-- Tags -->
    <div>
      <h3 class="text-zinc-400 text-sm font-semibold uppercase tracking-widest mb-4">Tags</h3>
      <div class="flex flex-wrap gap-2">
        <span v-for="tag in tags" :key="tag"
          class="px-3 py-1 rounded-lg text-xs font-semibold bg-zinc-800 text-zinc-300 hover:bg-pink-500/20 hover:text-pink-400 hover:border-pink-500/30 border border-zinc-700 cursor-pointer transition-all">
          {{ tag }}
        </span>
      </div>
    </div>

  </div>
</template>

<script setup>
const tags = ['Vue', 'React', 'Tailwind', 'JavaScript', 'CSS', 'HTML', 'Vite', 'Design', 'UI/UX', 'Frontend']
</script>