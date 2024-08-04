<script setup>
const category = "Waffle";
const name = "Waffle with Berries";
const price = 6.5;
</script>

<template>
  <article class="product-card">
    <img class="product-card__image" src="#" :alt="title" />
    <h3 class="product-card__category">{{ category }}</h3>
    <p class="product-card__name">{{ name }}</p>
    <p class="product-card__price">{{ price }}</p>

    <div class="product-card__action">
      <button class="product-card__button">Add to cart</button>
    </div>
  </article>
</template>
