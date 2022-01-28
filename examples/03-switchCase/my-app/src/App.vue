<template>
  <div id="app">
    <p>Today is:</p>
    <p>{{ today }}</p>
    <button @click="myFunction()">Which day</button>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from "vue-property-decorator";

@Component({})
export default class App extends Vue {
  public today: Date = new Date();

  myFunction(): void {
    switch (this.today.getDay()) {
      case 0:
        alert("Sunday");
        break;
      case 1:
        alert("Monday");
        break;
      case 2:
        alert("Tuesday");
        break;
      case 3:
        alert("Wednesday");
        break;
      case 4:
        alert("Thursday");
        break;
      case 5:
        alert("Friday");
        break;
      case 6:
        alert("Saturday");
        break;
      default:
        alert("No information available for that day.");
        break;
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
