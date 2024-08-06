<script setup>
const props = defineProps({
  product: Object,
});
</script>

<template>
  <article class="product__card">
    <div class="product__image">
      <img :src="product.image.mobile" :alt="'picture of ' + product.name" />

      <div class="product__action">
        <button class="product__button">
          <svg
            xmlns="http://www.w3.org/2000/svg"
            width="21"
            height="20"
            fill="none"
            viewBox="0 0 21 20">
            <g fill="#C73B0F" clip-path="url(#a)">
              <path
                d="M6.583 18.75a1.25 1.25 0 1 0 0-2.5 1.25 1.25 0 0 0 0 2.5ZM15.334 18.75a1.25 1.25 0 1 0 0-2.5 1.25 1.25 0 0 0 0 2.5ZM3.446 1.752a.625.625 0 0 0-.613-.502h-2.5V2.5h1.988l2.4 11.998a.625.625 0 0 0 .612.502h11.25v-1.25H5.847l-.5-2.5h11.238a.625.625 0 0 0 .61-.49l1.417-6.385h-1.28L16.083 10H5.096l-1.65-8.248Z" />
              <path
                d="M11.584 3.75v-2.5h-1.25v2.5h-2.5V5h2.5v2.5h1.25V5h2.5V3.75h-2.5Z" />
            </g>
            <defs>
              <clipPath id="a">
                <path fill="#fff" d="M.333 0h20v20h-20z" />
              </clipPath>
            </defs>
          </svg>
          <span> Add to Cart </span>
        </button>
      </div>
    </div>

    <p class="product__category">{{ product.category }}</p>
    <h4 class="product__name">{{ product.name }}</h4>
    <p class="product__price">${{ product.price.toFixed(2) }}</p>
  </article>
</template>

<style lang="scss" scoped>
.product {
  &__card {
    width: 100%;
    color: $rose-900;

    &:hover {
      .product__image {
        img {
          border-color: $red;
        }
      }
    }
  }

  &__image {
    position: relative;
    margin-bottom: 1rem;

    img {
      width: 100%;
      border-radius: $radius-base;
      border: 2px solid transparent;
    }
  }

  &__action {
    min-width: 168px;
    width: fit-content;
    position: absolute;
    bottom: -12px;
    left: 50%;
    transform: translateX(-50%);
    z-index: 2;
  }

  &__button {
    background: $white;
    color: $rose-900;
    font-weight: 600;
    padding: 0.5rem 1.5rem;
    border: 2px solid $rose-300;
    border-radius: $radius-round;
    display: flex;
    align-items: center;
    gap: 0.5rem;
    cursor: pointer;
  }

  &__category {
    font-size: 0.85rem;
    color: $rose-400;
  }

  &__name {
    font-size: 1.02rem;
    font-weight: 600;
  }

  &__price {
    font-size: 1.02rem;
    font-weight: 600;
    color: $red;
  }
}
</style>
