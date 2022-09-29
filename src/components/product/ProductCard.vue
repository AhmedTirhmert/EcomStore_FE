<template>
  <div class="product-card">
    <div class="product-img">
      <img
        src="https://images.unsplash.com/photo-1596462502278-27bfdc403348?ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=80"
        alt="Product Image"
      />
    </div>
    <div class="product-infos">
      <div class="product-right">
        <div class="product-name">Product Name</div>
        <div class="product-desc">
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Quam
          doloremque!
        </div>
        <div class="product-reviews">
          <i class="fas fa-star review-checked"></i>
          <i class="fas fa-star review-checked"></i>
          <i class="fas fa-star review-checked"></i>
          <i class="fas fa-star"></i>
          <i class="fas fa-star"></i>
        </div>
      </div>
      <div class="product-left">
        <div class="product-price">
          22 <span class="product-currency">DH</span>
        </div>
        <a href="#" class="product-btn"><i class="fas fa-cart-plus"></i></a>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "ProductCard",
};
</script>

<style scopped>
.product-card {
  background-color: #fff;
  border-radius: 1em;
  max-width: 17em;
  min-width: 17em;
  overflow: hidden;
  margin-right: 1em;
  border: 1px solid rgba(0, 0, 0, 0.2);
  cursor: pointer;
  transition: 0.5s ease;
}
.product-card:hover {
  filter: drop-shadow(0 0 0.2em rgba(0, 0, 0, 0.5));
  border: none;
  transform: scale(103%);
}
.product-card:hover  .product-btn {
  transform: translateX(0px);
}
.product-img {
  height: 15em;
  width: 17em;
  overflow: hidden;
  border-top-left-radius: 1em;
  border-top-right-radius: 1em;
  background-position: center;
  background-size: cover;
}
.product-infos {
  display: flex;
  gap: 1em;
  padding: 1em 1em;
  justify-content: space-between;
  text-align: start;
}
.product-name {
  font-family: "Poppins";
  font-size: 1.1em;
  font-weight: bold;
  margin-bottom: 5px;
}
.product-desc {
  font-family: "Poppins";
  font-size: 0.85em;
  line-height: 16px;
  margin-bottom: 10px;
}
.product-reviews .review-checked {
  color: orange;
}
.product-price {
  font-family: "Poppins";
  font-size: 2.5em;
  font-weight: bold;
  position: relative;
  margin-right: 1rem;
}
.product-left {
  display: flex;
  flex-direction: column;
  justify-content: space-between;
}
.product-currency {
  position: absolute;
  margin-top: 0.7em;
  font-size: 0.5em;
  font-weight: bold;
  transform: rotate(90deg);
}
.product-btn {
  font-family: "Poppins";
  padding: 0.3em 1em;
  margin-left: auto;
  background-color: #D4A350;
  color: #fff;
  border-radius: 5px;
  filter: drop-shadow(3px 3px 0.2em rgba(0, 0, 0, 0.3));
  transform: translateX(100px);
  transition: 0.5s ease-in-out;
  max-width: fit-content;
}
</style>