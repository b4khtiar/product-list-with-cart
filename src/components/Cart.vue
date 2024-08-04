<template>
  <article class="cart">
    <h2 class="cart__title">Your Cart (0)</h2>
    <img
      class="cart__image--empty"
      src="/images/illustration-empty-cart.svg"
      alt="empty cart"
    />
    <p class="cart__text--empty">Your added items will appear here.</p>
  </article>
</template>

<style lang="scss" scoped>
.cart {
  background: $white;
  border-radius: $radius-base;
  padding: 1.5rem;
  display: flex;
  flex-direction: column;
  gap: 1rem;
  box-shadow: 1px 2px 12px lighten($rose-300, 20%);

  &__title {
    color: $red;
    margin-bottom: 0.5rem;
  }

  &__image--empty {
    width: 50%;
    margin: 0 auto;
  }

  &__text--empty {
    color: $rose-500;
    text-align: center;
    font-weight: 600;
    padding-bottom: 1rem;
  }
}
</style>
