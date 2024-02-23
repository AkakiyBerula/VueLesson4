<template>
  <div class="full-page-container" :class="{ 'dark-theme': isDarkTheme }">
    <v-btn class="theme-toggle-btn" @click="toggleTheme">
      <v-icon>{{ isDarkTheme ? 'mdi-weather-night' : 'mdi-weather-sunny' }}</v-icon>
    </v-btn>
    
    <div class="content">
      <HelloWorld msg="Hello!" />
      <FormEvent />

      <v-divider></v-divider>

      <ClickHandler />

      <v-divider></v-divider>

      <GenerateItems />

      <v-divider></v-divider>

      <Animation />

      <v-divider></v-divider>

      <FlexTable />

      <TimeHistory />
    </div>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue';
import TimeHistory from './components/TimeHistory.vue';
import FormEvent from './components/FormEvent.vue';
import ClickHandler from './components/ClickHandler.vue';
import GenerateItems from './components/GenerateItems.vue';
import Animation from './components/Animation.vue';
import FlexTable from './components/FlexTable.vue'

export default {
  name: "App",
  components: {
    HelloWorld,
    TimeHistory,
    FormEvent,
    ClickHandler,
    GenerateItems,
    Animation,
    FlexTable
  },
  data() {
    return {
      isDarkTheme: false
    };
  },
  methods: {
    toggleTheme() {
      this.isDarkTheme = !this.isDarkTheme;
    }
  }
}
</script>

<style scoped>
.full-page-container {
  width: 100%;
  height: 100vh;
  margin: 0;
  padding: 0;
}

.theme-toggle-btn {
  width: 40px;
  height: 40px;
  margin-left: 1.5%;
  margin-top: 15px;
  border-radius: 6px;
}

.dark-theme {
  background-color: #333;
  color: #fff;
}

.content {
  padding: 20px;
}

@media (min-width: 1024px) {
  .content {
    max-width: 960px;
    margin: 0 auto;
  }
}
</style>




