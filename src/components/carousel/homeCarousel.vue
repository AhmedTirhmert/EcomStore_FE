<template>
  <carousel
    class="vue-carousel"
    :autoplay="true"
    :autoplayHoverPause="true"
    :navigationEnabled="false"
    :paginationEnabled="false"
    :perPage="1"
  >
    <slide>
      <div class="slide-hero">
        <div class="slide-hero-content">
          <p class="slide-hero-title">Be natural, be beautiful, Be you</p>
          <p class="slide-hero-text">
            Lorem ipsum, dolor sit amet consectetur adipisicing elit. Possimus
            quia similique dolorem minima ab qui, cum asperiores.
          </p>
          <a href="" class="slide-hero-cta"
            >Order Now<i class="lni lni-arrow-right slide-hero-cta-icon"></i
          ></a>
        </div>
      </div>
    </slide>
    <slide>
      <div class="slide-hero">
        <div class="slide-hero-content">
          <p class="slide-hero-title">Beauty is Whatever Brings Perfect</p>
          <p class="slide-hero-text">
            Lorem ipsum, dolor sit amet consectetur adipisicing elit. Possimus
            quia similique dolorem minima ab qui, cum asperiores.
          </p>
          <a href="" class="slide-hero-cta"
            >Order Now<i class="lni lni-arrow-right slide-hero-cta-icon"></i
          ></a>
        </div>
      </div>
    </slide>
    <slide>
      <div class="slide-hero">
        <div class="slide-hero-content">
          <p class="slide-hero-title">Beauty Lies Within us.</p>
          <p class="slide-hero-text">
            Lorem ipsum, dolor sit amet consectetur adipisicing elit. Possimus
            quia similique dolorem minima ab qui, cum asperiores.
          </p>
          <a href="" class="slide-hero-cta"
            >Order Now<i class="lni lni-arrow-right slide-hero-cta-icon"></i
          ></a>
        </div>
      </div>
    </slide>
    <slide>
      <div class="slide-hero">
        <div class="slide-hero-content">
          <p class="slide-hero-title">Timeless Product. Timeless beauty</p>
          <p class="slide-hero-text">
            Lorem ipsum, dolor sit amet consectetur adipisicing elit. Possimus
            quia similique dolorem minima ab qui, cum asperiores.
          </p>
          <a href="" class="slide-hero-cta"
            >Order Now<i class="lni lni-arrow-right slide-hero-cta-icon"></i
          ></a>
        </div>
      </div>
    </slide>
  </carousel>
</template>

<script>
import { Carousel, Slide } from "vue-carousel";

export default {
  name: "HomeCarousel",
  components: { Carousel, Slide },
  data() {
    return {
      bgImages: [
        "https://images.unsplash.com/photo-1596462502278-27bfdc403348?ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=80",
        "https://images.unsplash.com/photo-1570172619644-dfd03ed5d881?ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&ixlib=rb-1.2.1&auto=format&fit=crop&w=750&q=80",
        "https://images.unsplash.com/photo-1534143826428-81fc61582afd?ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&ixlib=rb-1.2.1&auto=format&fit=crop&w=294&q=80",
        "https://images.unsplash.com/photo-1522335789203-aabd1fc54bc9?ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&ixlib=rb-1.2.1&auto=format&fit=crop&w=765&q=80",
      ],
    };
  },
  mounted() {
    const slides = document.getElementsByClassName("slide-hero");
    slides.forEach((slide, index) => {
      slide.style.backgroundImage = `url(${this.bgImages[index]})`;
    });
  },
};
</script>

<style scoped>
:root {
}
.vue-carousel {
  height: 60vh;
}
.slide-hero {
  position: relative;
  display: flex;
  background-position: center;
  background-size: cover;
  background-origin: center;
}
.slide-hero::after {
  content: "";
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-image: radial-gradient(
    circle,
    #427a41,
    #355e35,
    #294329,
    #1d2a1d,
    #101210
  );
  opacity: 50%;
  z-index: 0;
}
.slide-hero-content {
  align-items: center;
  color: white;
  display: flex;
  flex-direction: column;
  font-family: "Poppins";
  gap: 2em;
  height: 417px;
  justify-content: center;
  width: 100%;
  z-index: 1;
}
.slide-hero-title {
  font-size: 5em;
  font-family: "Caveat";
  font-weight: bold;
  z-index: 2;
  position: relative;
}
.slide-hero-title::before {
  content: "";
  position: absolute;
  top: 0;
  left: 0;
  background-image: url("../../assets/images/brush.svg");
  background-size: cover;
  z-index: -1;
  width: 100%;
  height: 90%;
}
.slide-hero-text {
  width: 50%;
  font-size: 1.5em;
  line-height: 1.15em;
}
.slide-hero-cta {
  display: block;
  background: wheat;
  padding: 1em 2em;
  border-radius: 3px;
  transition: 0.25s;
  color: #629460;
}
.slide-hero-cta:hover,
.slide-hero-cta:focus {
  box-shadow: 0 0.5em 0.7em -0.4em #72ce6f;
  transform: translateY(-0.7em);
}

.slide-hero-cta-icon {
  margin-left: 10px;
  margin-top: auto;
  margin-bottom: auto;
}
</style>