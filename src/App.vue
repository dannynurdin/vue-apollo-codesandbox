<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png" width="25%" />
    <add-post />
    <post-list />
  </div>
</template>

<script>
import PostList from "./components/PostList";
import AddPost from "./components/AddPost";

export default {
  name: "App",
  components: {
    PostList,
    AddPost,
  },
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
