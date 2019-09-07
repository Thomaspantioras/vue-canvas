<template>
  <div>
    <p v-for="car in 4" v-bind:key="car" ref="car"> I am car number {{car}}</p>
    <button @click="submit">View refs</button>
  </div>
</template>
<script>
export default {
  name: 'TestList',
  data(){
    return {
    }
  },
  methods: {
    submit(){
      console.log(this.$refs)
    }
  }
}
</script>