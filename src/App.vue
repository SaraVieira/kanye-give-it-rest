<template>
  <div id="app">
    <h1>Kanye give it some rest</h1>
    <Kanye />
  </div>
</template>

<script>
import Kanye from "./components/Kanye";

export default {
  name: "App",
  components: {
    Kanye
  }
};
</script>

<style>
body {
  background: url("https://uploads.codesandbox.io/uploads/user/8d35d7c1-eecb-4aad-87b0-c22d30d12081/meQe-sativa.png")
    repeat;
  margin: 0;
  padding: 0;
}

#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  max-width: 80%;
  width: 1100px;
  height: 100vh;
  margin: auto;
  display: flex;
  flex-direction: column;
  justify-content: center;
}
</style>
