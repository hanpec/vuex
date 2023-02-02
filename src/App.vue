<template>
  <div id="app">
    <button v-on:click="increment">UP</button>
    <h1>Count:{{ count }}</h1>
    <UserList></UserList>
  </div>
</template>

<script>

import UserList from './components/UserList.vue'

export default {
  name: 'app',
  methods: {
    increment: function () {
      this.$store.commit('increment')
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