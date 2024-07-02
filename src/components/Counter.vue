<template>
    <div>
      <h1>Counter</h1>
      <p>Current count: {{ currentCount }}</p>
      <button @click="increment">+</button>
      <button @click="decrement">-</button>
    </div>
  </template>
  
  <script>
  import { mapState, mapActions } from 'vuex'
  
  export default {
    computed: {
      ...mapState(['count']),
      currentCount() {
        return this.$store.getters.currentCount
      }
    },
    methods: {
      ...mapActions(['increment', 'decrement'])
    }
  }
  </script>