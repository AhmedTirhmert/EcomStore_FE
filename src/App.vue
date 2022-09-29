<template>
  <div id="app">
    <nav-bar />
    <router-view />
  </div>
</template>
<script>
export default {
  name: "app",
  components: {
    NavBar: () => import("@/components/heading/NavBar"),
  },
};
</script>

<style>
@import url("https://fonts.googleapis.com/css2?family=Poppins:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,100;1,200;1,300;1,400;1,500;1,600;1,700;1,800;1,900&display=swap");
@import url("https://fonts.googleapis.com/css2?family=Caveat:wght@400;600;700&display=swap");
@import url("https://fonts.googleapis.com/css2?family=Merriweather+Sans:ital,wght@0,300,4,400,0,500;0,600;0,700;0,800;1,500;1,700&display=swap");
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
ul {
  list-style: none;
}
a {
  color: inherit;
  text-decoration: none;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
body::-webkit-scrollbar {
  width: 8px;
}

body::-webkit-scrollbar-track {
  box-shadow: #fff;
  background-color: #d8d8d8;
}

body::-webkit-scrollbar-thumb {
  background-color: #a8a4a4;
  border-radius: 15px;
}
</style>
