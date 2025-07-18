<script setup lang="ts">
const getRandomArbitrary = (min: number, max: number) => {
  return Math.random() * (max - min) + min
}
const getArray = (length: number) => {
  return Array.from({ length }, (_, i) => i + 1)
}
</script>

<template>
  <div
    class="break-inside-avoid rounded-md border border-amber-800/60 bg-amber-800/10 p-1 shadow-md"
  >
    <div
      class="font-ebgaramond inset-shadow-md relative rounded-md border border-amber-800/60 bg-amber-800/15 p-3 text-lg text-amber-950"
    >
      <h1
        class="font-unifrakturmaguntia z-10 text-center text-xl text-rose-800 text-shadow-md sm:text-2xl md:text-3xl"
      >
        Dungeons & Dragons
      </h1>
      <h2 class="mt-1 text-center text-xl font-bold text-amber-900 text-shadow-sm">GEAR</h2>
      <div class="mt-3 flex items-center justify-between">
        <span>Giocatori:</span>
        <span>5/6</span>
      </div>
      <div class="mt-3 flex items-center justify-between">
        <span>Orario:</span>
        <span>21:00</span>
      </div>
      <div class="mt-3">
        <span>Partecipanti:</span>
        <ul class="mt-1 grid list-none grid-cols-1 gap-2">
          <li
            v-for="i in getArray(getRandomArbitrary(1, 6))"
            :key="i"
            class="flex items-center justify-between"
          >
            <button
              class="w-full cursor-pointer rounded-md border border-amber-800/60 p-2 hover:bg-amber-200/15"
              @click="console.log('ciao')"
            >
              Giocatore {{ i }}
            </button>
          </li>
        </ul>
      </div>
    </div>
  </div>
</template>
