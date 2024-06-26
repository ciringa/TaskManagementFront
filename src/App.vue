<script>
    import  Header from "./components/header.vue"
    import Body from "./components/body.vue"
    export default{
      name:"App",
      components:{
        Header,
        Body
      },
      data(){
        return{
          list:["um","dois","tres"]
        }
      }
    }
</script>



<template>
    <Header />
    <Body Bound="sex" />
</template>


<style scoped >
</style>
