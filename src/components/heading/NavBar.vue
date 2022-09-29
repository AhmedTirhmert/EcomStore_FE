<template>
  <nav>
    <ul class="navbar">
      <li class="navbar-item logo">
        <a href="#"
          ><img src="@/assets/images/facebook_cover_photo_1.png" alt="logo"
        /></a>
      </li>
      <li class="navbar-item navbar-link"><a href="">Home</a></li>
      <li class="navbar-item navbar-link"><a href="">Trending</a></li>
      <li class="navbar-item navbar-link"><a href="">Hot sales</a></li>
      <li class="navbar-item navbar-link"><a href="">Top sales</a></li>
      <li class="navbar-item navbar-link"><a href="">Cart</a></li>
    </ul>
  </nav>
</template>

<script>
export default {
  name: "NavBar",
  props: {},
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
nav {
  background: #629460;
  color: white;
  z-index: 100;
}

.navbar {
  font-family: "Merriweather Sans";
  font-style: italic;
  font-size: 1.2rem;
  font-weight: lighter;
  padding: 0.5em;
  display: flex;
  justify-content: flex-end;
  margin-right: 5em;
  margin-left: 5em;
}
.logo {
  margin-right: auto;
  margin-left: 0 !important;
}
.navbar .logo img {
  height: 40px;
  border-radius: 2em;
}
.navbar-link {
  margin-left: 2.5em;
  align-self: center;
}
a {
  display: inline-block;
  text-decoration: none;
  color: inherit;
  position: relative;
}
.navbar-link a::after {
  content: "";
  position: absolute;
  bottom: -1.1em;
  left: 0;
  width: 0%;
  height: 0.2em;
  background-color: white;
  transition: ease-in-out 0.2s;
  display: block;
}
a:hover::after {
  width: 100%;
  left: 0;
}
</style>
