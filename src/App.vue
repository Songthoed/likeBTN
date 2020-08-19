<template>
  <div id="app">
    <div class>
      <h1>Please Like me</h1>
    </div>
    <div class="row">
      <div class="col-12">
        <img src="../public/img/myself.jpg" class="img-thumbnail" height="20%" width="20%" />
        <HelloWorld msg="ora!" />
        <Button />
      </div>
    </div>
    <div class="row">
      <div class="col-12">
        <img src="../public/img/36.jpg" class="img-thumbnail" height="20%" width="20%" />
        <HelloWorld msg="muda!" />
        <Button />
      </div>
    </div>
    <div class="row">
      <div class="col-12">
        <img src="../public/img/34.jpg" class="img-thumbnail" height="20%" width="20%" />
        <HelloWorld msg="help~" />
        <Button />
      </div>
    </div>
    <div class="row">
      <div class="col-12">
        <fontsize @cc="sum" />
        font size = {{total}}
      </div>
    </div>
    <div class="row">
      <div class="col-12">
        name
        <input type="text" v-model="name" />
        ID
        <input type="number" v-model="id" />
        GPA
        <input type="number" v-model="grade" step="0.01" />
      </div>
    </div>
    <div class="row">
      <div class="col-12">
        Name{{name}}
        ID{{id}}
        GPA:{{grade}}
      </div>
    </div>
  </div>
</template>

<script>
import HelloWorld from "./components/HelloWorld.vue";
import Button from "./components/Button.vue";
import fontsize from "./components/fontsize";
export default {
  name: "App",
  components: {
    HelloWorld,
    Button,
    fontsize,
  },
  data: function () {
    return {
      total: 0,
      name: "...",
      id: "...",
      grade: "...",
    };
  },
  methods: {
    sum(fsizevalue) {
      this.total = fsizevalue;
    },
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
