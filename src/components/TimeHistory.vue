<template>
  <v-container>
    <v-btn @click="saveEvent">Зберегти час</v-btn>

    <v-list>
      <v-subheader>Збережений час натискання:</v-subheader>
      <p>{{ timeSets }}</p>
      <v-list-item v-for="timeSet in timeSets" :key="timeSet" class="event-item">
        {{ timeSet }}
      </v-list-item>
    </v-list>
  </v-container>
</template>

<script>
export default {
  name: "TimeHistory",
  data() {
    return {
      timeSets: []
    };
  },
  methods: {
    saveEvent() {
      const currentTime = new Date().toLocaleString();
      this.timeSets.push(currentTime);
    }
  }
};
</script>

<style>
.event-item {
  padding: 8px;
}
</style>

