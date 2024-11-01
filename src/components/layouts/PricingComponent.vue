<script setup lang="ts"></script>

<template>
  <div class="pricing-container container">
    <div class="pricing-header" id="pricing">
      <h2>Pricing</h2>
      <h4>
        Most calendars are designed for teams.<br /><span>Slate is designed for freelancers</span>
      </h4>
    </div>
    <div class="price-table-container">
      <div class="price-table-item">
        <h3>FREE</h3>
        <h6>Organize across all apps by hand</h6>
        <div class="price">
          <h1>0</h1>
          <div>
            <h3>$</h3>
            <h6>Per Month</h6>
          </div>
        </div>
        <div class="feature-list">
          <ul>
            <li>Pricing Feature</li>
            <li>Pricing Feature</li>
            <li>Pricing Feature</li>
            <li>Pricing Feature</li>
            <li>Pricing Feature</li>
          </ul>
        </div>
        <button type="button">Order Now</button>
      </div>
      <div class="price-table-item inverse">
        <div class="item-header">
          <h3>FREE</h3>
          <h6>Organize across all apps by hand</h6>
        </div>
        <div class="price">
          <h1>10</h1>
          <div>
            <h3>$</h3>
            <h6>Per Month</h6>
          </div>
        </div>
        <div class="feature-list">
          <ul>
            <li>Pricing Feature</li>
            <li>Pricing Feature</li>
            <li>Pricing Feature</li>
            <li>Pricing Feature</li>
            <li>Pricing Feature</li>
          </ul>
        </div>
        <button type="button">Order Now</button>
      </div>
      <div class="price-table-item">
        <h3>FREE</h3>
        <h6>Organize across all apps by hand</h6>
        <div class="price">
          <h1>99</h1>
          <div>
            <h3>$</h3>
            <h6>Per Month</h6>
          </div>
        </div>
        <div class="feature-list">
          <ul>
            <li>Pricing Feature</li>
            <li>Pricing Feature</li>
            <li>Pricing Feature</li>
            <li>Pricing Feature</li>
            <li>Pricing Feature</li>
          </ul>
        </div>
        <button type="button">Order Now</button>
      </div>
    </div>
  </div>
</template>

<style scoped lang="scss">
@import '@/assets/breakpoints.scss';

.pricing-container {
  margin-top: 5rem;
  padding-top: 5rem;
  padding-bottom: 5rem;
  background-color: var(--color-background-dark);
  text-align: center;

  .pricing-header {
    padding: 0 2rem;
    h2,
    h4 {
      color: var(--color-text-light);
      span {
        display: none;
        @include media-breakpoint-up(md) {
          display: inline;
        }
      }
    }
  }

  .price-table-container {
    display: flex;
    flex-direction: column;
    width: 100%;
    gap: 4rem;
    color: var(--color-text);
    justify-content: center;
    align-items: center;
    margin-top: 4rem;

    @include media-breakpoint-up(lg) {
      flex-direction: row;
    }

    .price-table-item {
      background-color: var(--color-text-light);
      border-radius: 10px;
      border: 1px solid #dedede;
      padding: 40px;
      box-shadow: 1px 1px 4px var(--color-primary);

      &.inverse {
        background-color: var(--color-primary);
        color: var(--color-text-light);
        border-color: var(--color-primary);

        @include media-breakpoint-up(lg) {
          padding-top: 80px;
          padding-bottom: 80px;
        }

        h1,
        h3,
        h6 {
          color: var(--color-text-light);
        }

        button {
          background-color: var(--color-text-light);
          color: var(--color-primary);
        }
      }

      h1,
      h3,
      h6 {
        margin: 0;
        padding: 0;
      }

      .price {
        display: flex;
        align-items: flex-start;
        justify-content: center;
        gap: 8px;
        margin: 3rem 0;

        div {
          text-align: left;
          padding-top: 10px;
        }
      }

      .feature-list {
        margin-bottom: 3rem;
        ul {
          display: flex;
          flex-direction: column;
          gap: 1.5rem;
        }
      }

      button {
        width: 100%;
      }
    }
  }
}
</style>
