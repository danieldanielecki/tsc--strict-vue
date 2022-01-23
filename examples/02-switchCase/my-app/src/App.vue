<template>
  <div id="app">
    <p>Value of string:</p>
    <p>{{ myString }}</p>
    <button @click="myFunction()">Click me</button>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from "vue-property-decorator";

@Component({})
export default class App extends Vue {
  public myString = "";

  public myFunction(): void {
    console.log("myFunction with timeout of 3 seconds...");
    this.myString = "myFunction with timeout of 3 seconds...";
    setTimeout(this.myFunction2, 3000);
  }

  public myFunction2(): void {
    console.log("myFunction2");
    this.myString = "myFunction2";
    try {
      console.log("try");
      this.myString = "try";
    } catch (err) {
      // if (err instanceof Error) {
      console.log(err.message);
      this.myString = err.message;
      // }
    }
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
