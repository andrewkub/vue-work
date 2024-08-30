<template>
  <div class="counter">
    <counter-button @action="decrement"> - </counter-button>

    <counter-value :value="count"></counter-value>

    <counter-button @action="increment"> + </counter-button>
  </div>
</template>

<script setup>
import { ref } from 'vue'
import CounterButton from './CounterButton.vue'
import CounterValue from './CounterValue.vue'

const count = ref(0)

/* Метод уменьшения значения */
const decrement = () => {
  count.value -= 1
}

/* Метод увеличения значения */
const increment = () => {
  count.value += 1
}
</script>

<style lang="scss" scoped>
.counter {
  display: flex;
  align-items: center;
}
</style>
