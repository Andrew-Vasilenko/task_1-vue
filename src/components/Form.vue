<template>
    <Group v-bind:title = "serverResponse.title">
        <BoldString
            v-for = "arrElement in serverResponse.values"
            v-bind:value = "arrElement"
            v-bind:key = "arrElement.values"
        />
    </Group>
</template>

<script>
import Group from "@/components/FormElements/Group"
import BoldString from "@/components/FormElements/BoldString"

export default{
    props: ['serverResponse'],
    components: {
        Group:Group,
        BoldString:BoldString
    }    
}
</script>


<style scoped>
    strong {
        margin: 1%;
    }
</style>