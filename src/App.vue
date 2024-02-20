<template>

  <div>
    <HelloWorld msg="Hello!" />
  </div>
</template>

<script>

import HelloWorld from './components/HelloWorld.vue'

export default {
  name: "App",
  components: {
    HelloWorld
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
