<template>
    <h3 v-on:click = "toggleFormVisibility">{{ title }}</h3>
    <div>
        <slot v-if="isVisible"></slot>
    </div>
</template>

<script>
export default {  
    data () {
        return {
            isVisible: true
        }
    },  
    props: ['title'],
    methods: {
        toggleFormVisibility() {
            this.isVisible = !this.isVisible
        }
    }
}
</script>

<style scoped>
    h3 {
        background-color: white;
    }

    div {
        display: block;
        background-color: rgb(189, 224, 238);
        margin-top: 1%;
    }
</style>