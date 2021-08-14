<template>
  <div class="hello">
    <h1>{{title}} {{isAdmin}} </h1>
   <p>Followers:{{count}} </p>
   <button class="btn btn-primary m-2" @click="count++" >Increase</button>
   <button class="btn btn-primary m-2" @click="Decrease()" >Decrease</button>
   <button class="btn btn-primary m-2" @click="count==0" >Reset</button>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    title: String,
  },
  data(){
    return{
      count:0,
      isAdmin: true
    }
  },
  methods:{
    Decrease(){
      this.count -=1
    }
  },
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" scoped>
  h1{
    color:red;
    &:hover{
      color:green;
    }
  }
</style>
