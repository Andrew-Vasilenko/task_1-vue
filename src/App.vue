<template>
  <div>
    <Form
      v-for = "arrElement in serverResponses"
      v-bind:serverResponse = "arrElement"
      v-bind:key = "arrElement.values"
    />
  </div>
</template>

<script>
import Form from "@/components/Form"

export default {
  name: 'App',
  data () {
    return {
      serverResponses: [
        { title: "Заголовок1", values: ["<сложные аббревиатуры>", "Полное наименование"] },
        { title: "Заголовок2", values: ["<сложные аббревиатуры>", "Полное наименование"] }
      ]
    }
  },
  components: {
    Form:Form
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
