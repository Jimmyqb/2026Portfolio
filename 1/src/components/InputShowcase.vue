<template>
  <div class="space-y-8">

    <!-- Basic Inputs -->
    <div>
      <h3 class="text-zinc-400 text-sm font-semibold uppercase tracking-widest mb-4">Basic</h3>
      <div class="flex flex-col gap-4 max-w-sm">
        <input
          type="text"
          placeholder="Default input"
          class="bg-zinc-900 border border-zinc-700 rounded-xl px-4 py-3 text-white placeholder-zinc-500 outline-none focus:border-pink-500 transition-all" />
        <input
          type="email"
          placeholder="Email address"
          class="bg-zinc-900 border border-zinc-700 rounded-xl px-4 py-3 text-white placeholder-zinc-500 outline-none focus:border-pink-500 transition-all" />
        <input
          type="password"
          placeholder="Password"
          class="bg-zinc-900 border border-zinc-700 rounded-xl px-4 py-3 text-white placeholder-zinc-500 outline-none focus:border-pink-500 transition-all" />
      </div>
    </div>

    <!-- States -->
    <div>
      <h3 class="text-zinc-400 text-sm font-semibold uppercase tracking-widest mb-4">States</h3>
      <div class="flex flex-col gap-4 max-w-sm">
        <div>
          <input
            type="text"
            value="Valid input"
            class="w-full bg-zinc-900 border border-emerald-500 rounded-xl px-4 py-3 text-white outline-none transition-all" />
          <p class="text-emerald-400 text-xs mt-1.5 ml-1">Looks good!</p>
        </div>
        <div>
          <input
            type="text"
            value="Invalid input"
            class="w-full bg-zinc-900 border border-red-500 rounded-xl px-4 py-3 text-white outline-none transition-all" />
          <p class="text-red-400 text-xs mt-1.5 ml-1">This field is required.</p>
        </div>
        <input
          type="text"
          placeholder="Disabled input"
          disabled
          class="w-full bg-zinc-800 border border-zinc-700 rounded-xl px-4 py-3 text-zinc-500 cursor-not-allowed outline-none" />
      </div>
    </div>

    <!-- Form Example -->
    <div>
      <h3 class="text-zinc-400 text-sm font-semibold uppercase tracking-widest mb-4">Form Example</h3>
      <div class="bg-zinc-900 border border-zinc-800 rounded-2xl p-6 max-w-sm">
        <h4 class="font-black text-white text-lg mb-5">Create Account</h4>
        <div class="flex flex-col gap-4">
          <input
            type="text"
            placeholder="Full name"
            class="bg-zinc-950 border border-zinc-700 rounded-xl px-4 py-3 text-white placeholder-zinc-500 outline-none focus:border-pink-500 transition-all" />
          <input
            type="email"
            placeholder="Email address"
            class="bg-zinc-950 border border-zinc-700 rounded-xl px-4 py-3 text-white placeholder-zinc-500 outline-none focus:border-pink-500 transition-all" />
          <input
            type="password"
            placeholder="Password"
            class="bg-zinc-950 border border-zinc-700 rounded-xl px-4 py-3 text-white placeholder-zinc-500 outline-none focus:border-pink-500 transition-all" />
          <button class="cursor-pointer w-full py-3 rounded-xl font-bold bg-pink-500 hover:bg-pink-400 text-white transition-all">
            Sign Up
          </button>
          <p class="text-zinc-500 text-xs text-center">Already have an account? <span class="text-pink-400 cursor-pointer hover:text-pink-300">Log in</span></p>
        </div>
      </div>
    </div>

  </div>
</template>