<template>
  <v-container>
    <v-btn 
      @click="makeAnimation" 
      color="success">
      Змінити стиль квадрата
    </v-btn>
    <button ></button>
    <div class="animated-box" :class="{ 'animate': isAnimated }"></div>
  </v-container>
</template>

<script>
export default {
  data() {
    return {
      isAnimated: false
    };
  },
  methods: {
    makeAnimation() {
      this.isAnimated = !this.isAnimated;
    }
  }
};
</script>

<style scoped>
.animated-box {
  width: 100px;
  height: 100px;
  background-color: red;
  transition: all 0.5s ease;
}

.animate {
  transform: translateX(200px);
  background-color: blue;
  width: 150px;
  height: 150px; 
}
</style>






