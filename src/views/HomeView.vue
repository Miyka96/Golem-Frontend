<script setup lang="ts">
import TableCard from '@/components/TableCard.vue'
</script>

<template>
  <main class="h-screen py-10">
    <section class="columns-1 gap-4 space-y-6 p-6 sm:columns-2 lg:columns-3 lg:gap-6 xl:columns-4">
      <TableCard v-for="i in 6" :key="i"/>
    </section>
  </main>
</template>
