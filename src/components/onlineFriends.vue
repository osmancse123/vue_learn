<template>
    <div id="onlineFriends">
        <h2>Online Friends</h2>
        <div v-for="(row,index) in friend" :key="index">
            <h3 v-if="row.online">{{ row.name }}</h3>
        </div>
    </div>
</template>


<script>
export default {
    name: 'onlineFriends',
    props: ['friend'],
    data() {
        return {
            
        }
    }

}
</script>


<style scoped>
h3 {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: rgb(3, 209, 3);
  margin-top: 0px;
}
</style>