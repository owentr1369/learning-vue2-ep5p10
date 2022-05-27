<template>
  <div id="app">
    <h1>{{ title }}</h1>
    <HelloVn />
    <button @click="title = 'Changed with event click'">Update</button>
    <button @click="destroyEvent">Destroy</button>
  </div>
</template>

<script>
// v-if se remove phan tu di, con v-show se an phan tu di
import HelloVn from "./components/HelloVn.vue";
export default {
  name: "App",
  components: { HelloVn },
  data() {
    return { title: "VueJS instance lifecycle" };
  },
  methods: {
    destroyEvent: function () {
      this.$destroy();
    },
  },
  beforeCreate: function () {
    //
    console.log("beforeCreate!");
  },
  created: function () {
    //
    console.log("created!");
  },
  beforeMount: function () {
    //
    console.log("beforeMount!");
  },
  mounted: function () {
    //
    console.log("mounted!");
  },
  beforeUpdate: function () {
    //
    console.log("beforeUpdate!");
  },
  updated: function () {
    //
    console.log("updated!");
  },
  beforeDestroy: function () {
    //
    console.log("beforeDestroy!");
  },
  destroyed: function () {
    //
    console.log("destroyed!");
  },
};
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
