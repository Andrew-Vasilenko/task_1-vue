<template>
    <div>
        <h3
            v-on:click = "toggleFormVisibility"
        >{{ serverResponse.title }}</h3>
        <Form
            v-bind:values = "serverResponse.values"
            v-if = "isVisible"
        />
    </div>    
</template>

<script>
import Form from "@/components/Form"

export default {
    data () {
        return {
            isVisible: true
        }
    },
    props: ['serverResponse'],
    components: {
        Form:Form
    },
    methods: {
        toggleFormVisibility() {
            this.isVisible = !this.isVisible
        }
    }
}
</script>