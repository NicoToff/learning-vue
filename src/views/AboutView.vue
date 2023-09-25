<script lang="ts">
import CounterComponent from "@/components/CounterComponent.vue";
export default {
  components: {
    CounterComponent,
  },
};
</script>

<template>
  <div class="about">
    <h2>Welcome to your Playground!</h2>
    <h3>Powerful counter</h3>
    <p>
      Thanks to creative design and the power of JavaScript, your browser can now count the number of times
      you clicked this button. This revolutionary technology has <strong>countless work hours</strong> behind
      it. Enjoy it to its fullest!
    </p>
    <CounterComponent center />
  </div>
</template>

<style>
.about {
  line-height: normal;
}

.about p {
  line-height: 1.5rem;
  padding-bottom: 1rem;
}

.about > h2 {
  color: var(--vue-green);
  font-size: xx-large;
  font-weight: 600;
  padding-bottom: 1rem;
  padding-top: 1rem;
}

.about > h3 {
  color: var(--vue-green);
  font-size: x-large;
  font-weight: 400;
  text-decoration-line: underline;
  text-underline-offset: 6px;
  padding-bottom: 12px;
}

@media (min-width: 1024px) {
  .about {
    display: flex;
    flex-direction: column;
    justify-content: center;
  }
  .about > h2 {
    padding-top: 0;
  }
}
</style>
