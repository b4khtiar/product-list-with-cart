<script setup>
import Cart from "@/components/Cart.vue";
import ProductCard from "@/components/ProductCard.vue";
</script>

<template>
  <main class="container">
    <h1 class="app-title">Desserts</h1>
    <div class="product">
      <div class="product__container">
        <ProductCard />
        <ProductCard />
        <ProductCard />
        <ProductCard />
        <ProductCard />
      </div>
      <Cart />
    </div>
  </main>
  <footer class="footer">
    <p class="footer__text">
      Challenge by
      <a
        class="footer__link"
        href="http://www.frontendmentor.io?ref=challenge"
        target="_blank"
        rel="noopener noreferrer"
        >Frontendmentor</a
      >
      Coded by
      <a
        class="footer__link"
        href="https://github.com/b4khtiar"
        target="_blank"
        rel="noopener noreferrer"
        >Bakhtiar</a
      >.
    </p>
  </footer>
</template>

<style lang="scss" scoped>
.app-title {
  font-size: 2.6rem;
  margin-bottom: 2rem;
}

.footer {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 80px;
  padding: 0 1rem;

  &__text {
    font-size: 14px;
  }

  &__link {
    color: $green;
  }
}
</style>
