<template>
  <div>
    <h2>Hello this is for refs man!</h2>
    <p>You have counted {{this.counter}} times</p>
    <input type="text" ref="input">
    <button @click="submit">Add 1 to counter</button>
  </div>
</template>
<script>
export default {
  name: 'Test',
  data(){
    return {
      counter: 0
    }
  },
  methods: {
    submit(){
      this.counter++;
      console.log(this.$refs)
      console.log("this is the dom element:", this.$refs.input)
      console.log("this is the value:", this.$refs.input.value)
      console.log("this is the element's url:", this.$refs.input.baseURI)
    }
  }
}
</script>
<style scoped>
p , input, button{
  font-size: 30px;
}
input, button{
  font-size: 20px;
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
</style>
