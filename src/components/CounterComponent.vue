<script setup lang="ts">
import { ref } from "vue";
export type CounterComponentProps = {
  center?: boolean;
};
const count = ref(0);
const { center } = defineProps<CounterComponentProps>();
</script>

<template>
  <button :class="center ? 'btn-center' : ''" @click="count++">
    You clicked: {{ count }} time{{ count === 1 ? "" : "s" }}
  </button>
</template>

<style scoped>
button {
  border: 2px solid var(--vue-green);
  margin: 0;
  padding: 5px 10px 5px 10px;
  border-radius: 5px;
  width: fit-content;
  overflow: visible;
  text-align: inherit;
  background: var(--vue-gray);
  cursor: pointer;

  /* inherit font & color from ancestor */
  color: inherit;
  font: inherit;
  font-weight: 600;

  /* Normalize `line-height`. Cannot be changed from `normal` in Firefox 4+. */
  line-height: normal;

  /* Corrects font smoothing for webkit */
  -webkit-font-smoothing: inherit;
  -moz-osx-font-smoothing: inherit;

  /* Corrects inability to style clickable `input` types in iOS */
  -webkit-appearance: none;
}

button:focus {
  outline-offset: 3px;
}

button.btn-center {
  margin: 0 auto;
  display: block;
}
</style>
