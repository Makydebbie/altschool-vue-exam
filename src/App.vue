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

.container {
  padding: 0 50px;
}

.heading {
  border-bottom: 1px solid #e3e3e3;
  padding-bottom: 10px;
}

.pill {
  display: flex;
  justify-content: center;
  padding: 5px;
  border: 1px solid #e3e3e3;
  border-radius: 10px;
  margin: 5px;
}

.list-container {
  display: flex;
  flex-direction: row;
  flex-wrap: wrap;
}

.avatar {
  width: 50px;
  height: 50px;
}

</style>