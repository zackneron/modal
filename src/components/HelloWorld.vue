<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <input type="text" ref="name">
    <button @click="handleField">Click me</button>
    <h2 ref="output"></h2>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },
  methods: {
    handleField(){
      console.log(this.$refs.name.value)
      const text = this.$refs.name.value
      const output = this.$refs.output
      output.classList.add('primary')
      output.innerText = text
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}

.primary {
  color: blueviolet
}
</style>
