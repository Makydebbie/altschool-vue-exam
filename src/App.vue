<!-- <template>
  <div id="app">
  <router-view></router-view>
  <HelloWorld :msg="message" />
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'App',
  components: {
    HelloWorld
  },
  data(){
    return {
      message: "..."
    }
  },
  // methods: {
  //   alertMessage(){
  //     alert(this.message)
  //   }
  // }
}
</script> -->

<template>
  <div id="app">
    <router-view></router-view>
  </div>
</template>

<script type="text/javascript">
export default {
  name: 'App',
}
</script>

<style>
body {
  background-color: grey;
}


a:link, a:visited {

  background-color: white;
  color: black;
  padding: 14px 25px;
  text-align: center;
  text-decoration: underline;
  display: inline-block;
  border-radius: 10px;
  margin-bottom: 10px;
}

</style>