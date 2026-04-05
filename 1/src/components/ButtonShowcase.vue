<template>
  <div class="space-y-8">

    <!-- Variants -->
    <div>
      <h3 class="text-zinc-400 text-sm font-semibold uppercase tracking-widest mb-4">Variants</h3>
      <div class="flex flex-wrap gap-3">
        <button class="px-5 py-2.5 rounded-xl font-bold bg-pink-500 hover:bg-pink-400 text-white transition-all">
          Primary
        </button>
        <button class="px-5 py-2.5 rounded-xl font-bold bg-violet-500 hover:bg-violet-400 text-white transition-all">
          Secondary
        </button>
        <button class="px-5 py-2.5 rounded-xl font-bold bg-transparent border-2 border-pink-500 text-pink-500 hover:bg-pink-500 hover:text-white transition-all">
          Outline
        </button>
        <button class="px-5 py-2.5 rounded-xl font-bold text-pink-400 hover:text-pink-300 hover:bg-zinc-800 transition-all">
          Ghost
        </button>
      </div>
    </div>

    <!-- Sizes -->
    <div>
      <h3 class="text-zinc-400 text-sm font-semibold uppercase tracking-widest mb-4">Sizes</h3>
      <div class="flex flex-wrap items-center gap-3">
        <button class="px-3 py-1.5 rounded-lg text-xs font-bold bg-pink-500 hover:bg-pink-400 text-white transition-all">
          Small
        </button>
        <button class="px-5 py-2.5 rounded-xl text-sm font-bold bg-pink-500 hover:bg-pink-400 text-white transition-all">
          Medium
        </button>
        <button class="px-7 py-3.5 rounded-2xl text-base font-bold bg-pink-500 hover:bg-pink-400 text-white transition-all">
          Large
        </button>
      </div>
    </div>

    <!-- States -->
    <div>
      <h3 class="text-zinc-400 text-sm font-semibold uppercase tracking-widest mb-4">States</h3>
      <div class="flex flex-wrap gap-3">
        <button class="px-5 py-2.5 rounded-xl font-bold bg-pink-500 text-white transition-all flex items-center gap-2">
          <span class="w-4 h-4 border-2 border-white border-t-transparent rounded-full animate-spin"></span>
          Loading
        </button>
        <button disabled class="px-5 py-2.5 rounded-xl font-bold bg-zinc-700 text-zinc-500 cursor-not-allowed">
          Disabled
        </button>
      </div>
    </div>

  </div>
</template>