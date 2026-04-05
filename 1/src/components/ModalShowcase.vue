<template>
  <div class="space-y-8">

    <!-- Triggers -->
    <div>
      <h3 class="text-zinc-400 text-sm font-semibold uppercase tracking-widest mb-4">Try them out</h3>
      <div class="flex flex-wrap gap-3">
        <button @click="openModal('default')"
          class="cursor-pointer px-5 py-2.5 rounded-xl font-bold bg-pink-500 hover:bg-pink-400 text-white transition-all">
          Open Modal
        </button>
        <button @click="openModal('danger')"
          class="cursor-pointer px-5 py-2.5 rounded-xl font-bold bg-red-500 hover:bg-red-400 text-white transition-all">
          Danger Modal
        </button>
        <button @click="openModal('success')"
          class="cursor-pointer px-5 py-2.5 rounded-xl font-bold bg-emerald-500 hover:bg-emerald-400 text-white transition-all">
          Success Modal
        </button>
      </div>
    </div>

    <!-- Modal Overlay -->
    <Transition name="fade">
      <div v-if="activeModal"
        class="fixed inset-0 bg-black/70 backdrop-blur-sm flex items-center justify-center z-50"
        @click.self="closeModal">

        <!-- Default -->
        <div v-if="activeModal === 'default'"
          class="bg-zinc-900 border border-zinc-800 rounded-2xl p-8 w-full max-w-md mx-4 shadow-2xl">
          <h3 class="text-xl font-black text-white mb-2">Are you sure?</h3>
          <p class="text-zinc-400 text-sm mb-6">This action cannot be undone. Please confirm you want to proceed.</p>
          <div class="flex gap-3 justify-end">
            <button @click="closeModal"
              class="px-4 py-2 rounded-xl font-bold text-zinc-400 hover:text-white hover:bg-zinc-800 transition-all">
              Cancel
            </button>
            <button @click="closeModal"
              class="px-4 py-2 rounded-xl font-bold bg-pink-500 hover:bg-pink-400 text-white transition-all">
              Confirm
            </button>
          </div>
        </div>

        <!-- Danger -->
        <div v-if="activeModal === 'danger'"
          class="bg-zinc-900 border border-red-500/30 rounded-2xl p-8 w-full max-w-md mx-4 shadow-2xl">
          <div class="w-12 h-12 rounded-2xl bg-red-500/20 flex items-center justify-center mb-4">
            <span class="text-red-400 text-xl">⚠️</span>
          </div>
          <h3 class="text-xl font-black text-white mb-2">Delete Account</h3>
          <p class="text-zinc-400 text-sm mb-6">This will permanently delete your account and all your data. This cannot be reversed.</p>
          <div class="flex gap-3 justify-end">
            <button @click="closeModal"
              class="px-4 py-2 rounded-xl font-bold text-zinc-400 hover:text-white hover:bg-zinc-800 transition-all">
              Cancel
            </button>
            <button @click="closeModal"
              class="px-4 py-2 rounded-xl font-bold bg-red-500 hover:bg-red-400 text-white transition-all">
              Delete
            </button>
          </div>
        </div>

        <!-- Success -->
        <div v-if="activeModal === 'success'"
          class="bg-zinc-900 border border-emerald-500/30 rounded-2xl p-8 w-full max-w-md mx-4 shadow-2xl text-center">
          <div class="w-16 h-16 rounded-full bg-emerald-500/20 flex items-center justify-center mb-4 mx-auto">
            <span class="text-3xl">🎉</span>
          </div>
          <h3 class="text-xl font-black text-white mb-2">All Done!</h3>
          <p class="text-zinc-400 text-sm mb-6">Your changes have been saved successfully.</p>
          <button @click="closeModal"
            class="w-full px-4 py-2 rounded-xl font-bold bg-emerald-500 hover:bg-emerald-400 text-white transition-all">
            Continue
          </button>
        </div>

      </div>
    </Transition>

  </div>
</template>

<script setup>
import { ref } from 'vue'

const activeModal = ref(null)

const openModal = (type) => activeModal.value = type
const closeModal = () => activeModal.value = null
</script>

<style scoped>
.fade-enter-active, .fade-leave-active { transition: opacity 0.2s ease; }
.fade-enter-from, .fade-leave-to { opacity: 0; }
</style>