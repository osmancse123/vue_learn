<template>
    <div id="Hook">
        <h2>{{title}}</h2>
        <button @click="changeTitle">change</button>
    </div>
</template>


<script>
export default {
    name: 'Hook',
    data() {
        return {
            title: 'Hook Part'
        }
    },

    beforeCreate() {
        alert('before create')
    },
    created() {
        alert('created')
    },
    beforeUpdate() {
        alert('before Update')
    },
    updated() {
        alert('Updated')
    },

    methods: {
        changeTitle() {
            this.title = 'learn vue'
        }
    }

}
</script>


<style >

</style>