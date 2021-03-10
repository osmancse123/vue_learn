<template>
    <div id="bestfriend">
        <h2>All Friends</h2>
        <div v-for="(row,index) in fri" :key="index">
            <h4 @click="nufriends(row.name)">{{ row.name }}</h4>
        </div>
    </div>
</template>


<script>
export default {
    name: 'allFriends',
    props: ['fri'],
    data() {
        return {
            
        }
    }, 
    
    methods: {
        nufriends(name) {
            this.$emit('delete', {name})
        }
    }

}
</script>


<style scoped>
h4 {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 0px;
}
</style>