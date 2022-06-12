<template>
  <div id="app">
    <NavBar></NavBar>
  </div>
</template>

<style lang="scss">
* {
  margin: 0;
  background: #212529;
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  text-align: center;
}
</style>
<script lang="ts">
// Dependencies
import Vue from "vue";
import Component from "vue-class-component";

// Components
import NavBar from "./components/NavBar.vue";

@Component({
  components: {
    NavBar,
  },
})
export default class App extends Vue {}
</script>
