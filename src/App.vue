<template>
  <div>
    <HelloWorld msg="Hello!" />
    <FormEvent />
    <TimeHistory />
  </div>
</template>

<script>

import HelloWorld from './components/HelloWorld.vue';
import TimeHistory from './components/TimeHistory.vue';
import FormEvent from './components/FormEvent.vue';

export default {
  name: "App",
  components: {
    HelloWorld,
    TimeHistory,
    FormEvent
  }
}
</script>


<style scoped>
header {
  line-height: 1.5;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

@media (min-width: 1024px) {

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }
}
</style>
