<template>
    <div>
        <Group
            v-on:click = "toggleFormVisibility"
            v-bind:title = "serverResponse.title"
        />
        <div v-if = "isVisible">
            <BoldString
                v-for = "arrElement in serverResponse.values"
                v-bind:value = "arrElement"
                v-bind:key = "arrElement.values"
            />
        </div>        
    </div>
</template>

<script>
import Group from "@/components/FormElements/Group"
import BoldString from "@/components/FormElements/BoldString"

export default{
    data () {
        return {
            isVisible: true
        }
    },
    props: ['serverResponse'],
    components: {
        Group:Group,
        BoldString:BoldString
    },
    methods: {
        toggleFormVisibility() {
            this.isVisible = !this.isVisible
        }
    }
}
</script>


<style scoped>
    div {
        display: block;
        background-color: rgb(189, 224, 238);
        margin-top: 1%;
    }

    strong {
        margin: 1%;
    }
</style>