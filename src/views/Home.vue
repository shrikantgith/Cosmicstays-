<template>
  <div class="home">
    <!-- <img alt="Vue logo" src="../assets/logo.png" id="logo"> -->
      <nav class="navbar navbar-light bg-light">
        <div class="container-fluid" id="mainnav">
          <a class="navbar-brand" href="#">
            <img src="../assets/logo.png" alt="" width="30" height="24" class="d-inline-block align-text-top">
            ToDoList
          </a>
        </div>
      </nav>
    <HelloWorld/>
    <Display />
  </div>
</template>
<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue'
import Display from '@/components/Display.vue'
export default {
  name: 'Home',
  components: {
    HelloWorld,
    Display
  }
}
</script>
<style scoped>
  #logo{
    width: 25px;
    height: 25px;
  }
  #mainnav{
    text-align: center;
  }
</style>
