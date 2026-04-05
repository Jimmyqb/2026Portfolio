<template>
  <div class="min-h-screen bg-zinc-950 text-white flex">

    <!-- Sidebar -->
    <aside class="w-56 bg-zinc-900 border-r border-zinc-800 p-6 flex flex-col gap-2 fixed h-full">
      <div class="mb-6">
        <h1 class="text-xl font-black text-pink-500">Vivid UI ⚡</h1>
        <p class="text-zinc-500 text-xs mt-1">Component Library</p>
      </div>

      <p class="text-zinc-600 text-xs uppercase tracking-widest font-semibold mb-1">Components</p>
      <a v-for="section in sections" :key="section.name"
        @click="active = section.name"
        :class="[
          'px-3 py-2 rounded-lg cursor-pointer text-sm font-medium transition-all flex items-center gap-2',
          active === section.name
            ? 'bg-pink-500 text-white'
            : 'text-zinc-400 hover:text-white hover:bg-zinc-800'
        ]">
        <span>{{ section.icon }}</span>
        {{ section.name }}
      </a>

      <div class="mt-auto">
        <p class="text-zinc-600 text-xs text-center">Built with Vue + Tailwind</p>
      </div>
    </aside>

    <!-- Main content -->
    <main class="ml-56 p-10 flex-1">
      <div class="max-w-3xl">
        <div class="mb-10">
          <div class="flex items-center gap-3 mb-2">
            <span class="text-3xl">{{ currentSection.icon }}</span>
            <h2 class="text-4xl font-black">{{ active }}</h2>
          </div>
          <p class="text-zinc-400">{{ currentSection.description }}</p>
        </div>

        <ButtonShowcase v-if="active === 'Buttons'" />
        <CardShowcase v-if="active === 'Cards'" />
        <BadgeShowcase v-if="active === 'Badges'" />
        <ModalShowcase v-if="active === 'Modals'" />
        <InputShowcase v-if="active === 'Inputs'" />
      </div>
    </main>

  </div>
</template>

<script setup>
import { ref, computed } from 'vue'
import ButtonShowcase from './components/ButtonShowcase.vue'
import CardShowcase from './components/CardShowcase.vue'
import BadgeShowcase from './components/BadgeShowcase.vue'
import ModalShowcase from './components/ModalShowcase.vue'
import InputShowcase from './components/InputShowcase.vue'

const sections = [
  { name: 'Buttons', icon: '🎯', description: 'Interactive button variants, sizes and states.' },
  { name: 'Cards', icon: '🃏', description: 'Flexible card layouts for displaying content.' },
  { name: 'Badges', icon: '🏷️', description: 'Labels, tags and status indicators.' },
  { name: 'Modals', icon: '🪟', description: 'Dialog windows for confirmations and alerts.' },
  { name: 'Inputs', icon: '✏️', description: 'Form inputs with validation states.' },
]

const active = ref('Buttons')
const currentSection = computed(() => sections.find(s => s.name === active.value))
</script>