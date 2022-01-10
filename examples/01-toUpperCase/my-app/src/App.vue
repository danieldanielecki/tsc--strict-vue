<template>
  <div id="app">
    <p>{{ stringValue }}</p>
    <p>{{ upperCaseString }}</p>
    <button @click="myFunction(2)">Click Me</button>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from "vue-property-decorator";

@Component({})
export default class App extends Vue {
  public stringValue = "My name is Daniel";
  public upperCaseString = "";

  myFunction(sampleParameter: string): void {
    this.upperCaseString = sampleParameter.toUpperCase();
  }
}
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
