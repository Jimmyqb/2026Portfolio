<template>
  <div class="space-y-8">

    <!-- Basic Card -->
    <div>
      <h3 class="text-zinc-400 text-sm font-semibold uppercase tracking-widest mb-4">Basic</h3>
      <div class="flex flex-wrap gap-5">
        <div class="bg-zinc-900 border border-zinc-800 rounded-2xl p-6 w-64 hover:border-pink-500 transition-all">
          <div class="w-10 h-10 rounded-xl bg-pink-500 mb-4"></div>
          <h4 class="font-bold text-white mb-1">Card Title</h4>
          <p class="text-zinc-400 text-sm">A simple card with an icon, title and description text.</p>
        </div>

        <div class="bg-zinc-900 border border-zinc-800 rounded-2xl p-6 w-64 hover:border-violet-500 transition-all">
          <div class="w-10 h-10 rounded-xl bg-violet-500 mb-4"></div>
          <h4 class="font-bold text-white mb-1">Another Card</h4>
          <p class="text-zinc-400 text-sm">Cards are great for grouping related content together.</p>
        </div>
      </div>
    </div>

    <!-- Profile Card -->
    <div>
      <h3 class="text-zinc-400 text-sm font-semibold uppercase tracking-widest mb-4">Profile</h3>
      <div class="flex flex-wrap gap-5">
        <div class="bg-zinc-900 border border-zinc-800 rounded-2xl p-6 w-64 flex flex-col items-center text-center">
          <div class="w-16 h-16 rounded-full bg-linear-to-br from-pink-500 to-violet-500 mb-3"></div>
          <h4 class="font-bold text-white">Alex Rivera</h4>
          <p class="text-zinc-400 text-sm mb-4">Frontend Developer</p>
          <button class="w-full px-4 py-2 rounded-xl bg-pink-500 hover:bg-pink-400 text-white text-sm font-bold transition-all">
            Follow
          </button>
        </div>
      </div>
    </div>

    <!-- Stat Cards -->
    <div>
      <h3 class="text-zinc-400 text-sm font-semibold uppercase tracking-widest mb-4">Stats</h3>
      <div class="flex flex-wrap gap-4">
        <div v-for="stat in stats" :key="stat.label"
          class="bg-zinc-900 border border-zinc-800 rounded-2xl p-5 w-40 hover:border-pink-500 transition-all">
          <p class="text-zinc-400 text-xs mb-1">{{ stat.label }}</p>
          <p class="text-2xl font-black" :class="stat.color">{{ stat.value }}</p>
        </div>
      </div>
    </div>

  </div>
</template>

<script setup>
const stats = [
  { label: 'Total Users', value: '24k', color: 'text-pink-400' },
  { label: 'Revenue', value: '$8.2k', color: 'text-violet-400' },
  { label: 'Growth', value: '+18%', color: 'text-emerald-400' },
  { label: 'Tickets', value: '142', color: 'text-amber-400' },
]
</script>