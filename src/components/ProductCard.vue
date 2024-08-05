<script setup>
const category = "Waffle";
const name = "Waffle with Berries";
const price = 6.5;
</script>

<template>
  <article class="product__card">
    <img class="product__image" src="#" :alt="'picture of ' + name" />
    <h3 class="product__category">{{ category }}</h3>
    <p class="product__name">{{ name }}</p>
    <p class="product__price">{{ price }}</p>

    <div class="product__action">
      <button class="product__button">Add to cart</button>
    </div>
  </article>
</template>

<style lang="scss" scoped>
.product {
  &__card {
    border: 1px solid gray;
  }
}
</style>
