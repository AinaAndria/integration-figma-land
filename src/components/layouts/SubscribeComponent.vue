<script setup lang="ts"></script>

<template>
  <div class="subscribe-container" id="subscribe">
    <div class="subscribe-start">
      <img src="@/assets/images/newletter.png" alt="newletter" />
    </div>
    <div class="subscribe-end">
      <div class="title">
        <h3>At your fingertips</h3>
        <h2 class="desktop">Lightning fast prototyping</h2>
        <h2 class="mobile">Newsletter</h2>
      </div>
      <img class="image-mobile" src="@/assets/images/newletter.png" alt="newletter" />
      <div class="form">
        <div class="form-header">
          <h3>Subscribe to our Newletter</h3>
          <p>Available exclusivery on Figmaland</p>
        </div>
        <div class="form-item">
          <input type="email" name="email" placeholder="Your Email" />
          <button type="button">Subscribe</button>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped lang="scss">
@import '@/assets/breakpoints.scss';

.subscribe-container {
  margin-top: 12rem;
  display: flex;
  gap: 2rem;

  .subscribe-start {
    flex: 1.5;
    display: none;
    @include media-breakpoint-up(xl) {
      display: block;
    }

    img {
      width: 100%;
    }
  }

  .subscribe-end {
    flex: 1;

    h3,
    p {
      margin: 0;
      padding: 0;
    }

    h2 {
      margin: 1rem 0;
    }

    .title {
      text-align: center;

      @include media-breakpoint-up(xl) {
        text-align: left;
      }

      .desktop {
        display: none;
        @include media-breakpoint-up(xl) {
          display: block;
        }
      }

      .mobile {
        @include media-breakpoint-up(xl) {
          display: none;
        }
      }
    }

    .image-mobile {
      width: 100%;
      @include media-breakpoint-up(xl) {
        display: none;
      }
      margin: 4rem 0;
    }

    .form {
      margin-top: 2rem;

      text-align: center;

      @include media-breakpoint-up(xl) {
        text-align: left;
      }

      .form-item {
        width: 100%;
        display: flex;
        align-items: stretch;
        flex-direction: column;
        margin-top: 1rem;
        gap: 12px;

        @include media-breakpoint-up(xl) {
          align-items: center;
          flex-direction: row;
        }

        input {
          flex: 1;
        }

        input,
        button {
          margin: 0;
          @include media-breakpoint-up(sm) {
            margin: 0 4rem;
          }
          @include media-breakpoint-up(lg) {
            margin: 0 6rem;
          }
          @include media-breakpoint-up(xl) {
            margin: 0;
          }
        }
      }
    }
  }
}
</style>
