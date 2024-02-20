<template>
  <v-container>
    <v-btn @click="handleClick">{{ buttonText }}</v-btn>
    <p>Натисни 5 разів, щоб викликати другий метод: {{ counter }}</p>
  </v-container>
</template>

<script>
export default {
  name: "ClickHandler",

  data() {
    return {
      condition: false,
      buttonText: 'Метод 1',
      counter: 0
    };
  },
  methods: {
    handleClick() {
      this.condition = this.checkCondition
      
      if (this.condition) {
        this.secondMethod();
      } else {
        this.firstMethod();
        this.counter++
      }

    },
    firstMethod() {
      console.log('Викликано метод 1');
    },
    secondMethod() {
      console.log('Викликано метод 2');
    }
  },
  computed: {
    checkCondition() {
      return this.counter >= 5 ? true : false
    }
  },
  watch: {
    condition(newValue) {
      this.buttonText = newValue ? 'Метод 2' : 'Метод 1';
    },
    counter(newValue, oldValue) {
      console.log(newValue, oldValue)
    }
  }
};
</script>

<style>

</style>



