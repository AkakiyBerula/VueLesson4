<template>
  <div>
    <HelloWorld msg="Hello!" />
    <FormEvent />

    <v-divider></v-divider>
    
    <ClickHandler />

    <v-divider></v-divider>

    <GenerateItems />

    <v-divider></v-divider>

    <Animation />

    <v-divider></v-divider>

    <TimeHistory />

  </div>
</template>

<script>

import HelloWorld from './components/HelloWorld.vue';
import TimeHistory from './components/TimeHistory.vue';
import FormEvent from './components/FormEvent.vue';
import ClickHandler from './components/ClickHandler.vue';
import GenerateItems from './components/GenerateItems.vue';
import Animation from './components/Animation.vue'

export default {
  name: "App",
  components: {
    HelloWorld,
    TimeHistory,
    FormEvent,
    ClickHandler,
    GenerateItems,
    Animation
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
