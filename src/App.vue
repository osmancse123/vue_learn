<template>
  <div id="app">
    <h2>{{ title }}</h2>
    <Navbar/>
    <allFriends :fri="friends" @delete="deletefriends"></allFriends>
    <onlineFriends :friend="friends" />
    <offlineFriends :friends="friends" />
    <Hook/>
  </div>
</template>

<script>
import Navbar from './components/navbar.vue'
import allFriends from './components/bestFriends.vue'
import onlineFriends from './components/onlineFriends.vue'
import offlineFriends from './components/offlineFriends.vue'
import Hook from './components/Hook.vue'

export default {
  name: 'App',
  data() {
    return {
      title: 'hurray ! Our vue apps are running :)',
      friends: [
                {name: 'A', online: true},
                {name: 'B', online: true},
                {name: 'C', online: false},
                {name: 'D', online: true},
                {name: 'E', online:false}
              ]
    }
  },
  components: {
    Navbar,
    allFriends,
    onlineFriends,
    offlineFriends,
    Hook
  },

  methods: {
    deletefriends(payload) {
      // console.log(payload);
      this.friends = this.friends.filter(friend => {
        return friend.name !== payload.name
      })
    }
  }
}
</script>

<style>
h2 {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
