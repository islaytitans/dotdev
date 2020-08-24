<template>
  <article class="p-5 grid items-center text-center">
    <h1 class="text-green-700 text-3xl font-bold">Jonathan Robbins</h1>
    <p>Let's do this</p>
    <p class="mt-2">
      <span class="block">Count is: {{ count }}</span>
      <button
        class="bg-green-700 hover:bg-green-500 text-white font-bold py-2 px-4 rounded"
        @click="increase"
      >
        Increment
      </button>
    </p>
  </article>
</template>

<script lang="ts">
import { defineComponent, ref } from 'vue'
export default defineComponent({
  setup() {
    const count = ref(0)
    const increase = () => {
      count.value++
    }

    return {
      count,
      increase,
    }
  },
})
</script>
