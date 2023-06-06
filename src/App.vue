<template>
  <div id="app">
    <button v-on:click="increment">UP</button>
    <h1>Count:{{ count }}</h1>
    <UserList></UserList>
    <button v-on:click="decrement">DOWN</button>
  </div>
</template>

<script>

import UserList from './components/UserList.vue'

export default {
  name: 'app',
  methods: {
    increment: function () {
      this.$store.commit('increment')
    },
    decrement: function () {
      this.$store.commit('decrement')
    }
  },
  computed: {
    count: function () {
      return this.$store.state.count
    }
  },
  components: {
    UserList
  }
}
</script>