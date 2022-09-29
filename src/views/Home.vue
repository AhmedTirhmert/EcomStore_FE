<template>
  <section class="home">
    <home-carousel />
    <hot-sales />
    <div class="featured-categories">
      <div class="category category-skin">
        <h2 class="category-title">Skin</h2>
        <p class="category-text">Get the best skin in the city.</p>
      </div>
      <div class="category category-hair">
        <h2 class="category-title">Hair</h2>
        <p class="category-text">Your hair is our canvas.</p>
      </div>
      <div class="category category-body">
        <h2 class="category-title">Body</h2>
        <p class="category-text">You're never too old to become younger.</p>
      </div>
      <div class="category category-accesories">
        <h2 class="category-title">Accesories</h2>
        <p class="category-text">
          Wear an unusual accessory to complete your outfit.
        </p>
      </div>
    </div>
  </section>
</template>

<script>
// @ is an alias to /src

export default {
  name: "Home",
  components: {
    HomeCarousel: () => import("@/components/carousel/homeCarousel.vue"),
    HotSales: () => import("@/components/hotSales.vue"),
  },
};
</script>

<style scoped>
.featured-categories {
  height: 100vh;
  display: grid;
  grid-template-columns: 6fr 6fr;
  gap: 1em;
  margin: auto 4rem auto 4rem;
}
.featured-categories .category {
  display: flex;
  flex-direction: column;
  background-position: center;
  background-size: cover;
  justify-content: center;
  position: relative;
  overflow: hidden;
  cursor: pointer;
  border-radius: 3px;
}
.featured-categories .category-title,
.featured-categories .category-text {
  color: white;
  z-index: 2;
}
.category-title {
  font-family: "Poppins";
  font-size: 3.4em;
}
.category-text {
  font-family: "Poppins";
  font-size: 1.1em;
}
.category-skin {
  background-image: url("https://images.unsplash.com/photo-1595514446083-236b9985a0e2?ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&ixlib=rb-1.2.1&auto=format&fit=crop&w=750&q=80");
}
.category-hair {
  background-image: url("https://images.unsplash.com/photo-1557353425-6c61136de070?ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&ixlib=rb-1.2.1&auto=format&fit=crop&w=751&q=80");
}
.category-body {
  background-image: url("https://images.unsplash.com/photo-1619451427882-6aaaded0cc61?ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&ixlib=rb-1.2.1&auto=format&fit=crop&w=334&q=80");
}
.category-accesories {
  background-image: url("https://images.unsplash.com/photo-1506630448388-4e683c67ddb0?ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&ixlib=rb-1.2.1&auto=format&fit=crop&w=334&q=80");
}
.featured-categories .category::before {
  content: "";
  width: 100%;
  height: 100%;
  position: absolute;
  top: 0;
  left: 0;
  background: linear-gradient(to top, #292e49, #536976, #bbd2c5);
  opacity: 0.8;
  /* mix-blend-mode: multiply; */
  /* transform: translateX(50%); */
  transition: 0.4s ease-in;
}
.category:hover .category::before {
  display: none;
}
</style>
