<template>
    <div id="offlineFriends">
        <h2>Offline Friends</h2>
        <div v-for="(row,index) in friends" :key="index">
            <h3 v-if="!row.online">{{ row.name }}</h3>
        </div>
    </div>
</template>


<script>
export default {
    name: 'offlineFriends',
    props: ['friends'],
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
  color: rgb(241, 15, 53);
  margin-top: 0px;
}
</style>