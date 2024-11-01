<script setup lang="ts"></script>

<template>
  <div class="partner-container">
    <div class="partner-header">
      <h2>Partners</h2>
      <h4>
        Most calendars are designed for teams.<br /><span>Slate is designed for freelancers</span>
      </h4>
    </div>
    <div class="logo-container">
      <div class="logo-item">
        <h6>Client Name</h6>
        <img src="@/assets/images/logo/google.png" alt="google" />
      </div>
      <div class="logo-item">
        <h6>Client Name</h6>
        <img src="@/assets/images/logo/amazon.png" alt="amazon" />
      </div>
      <div class="logo-item">
        <h6>Client Name</h6>
        <img src="@/assets/images/logo/microsoft.png" alt="microsoft" />
      </div>
      <div class="logo-item tablet-only">
        <h6>Client Name</h6>
        <img src="@/assets/images/logo/uber.png" alt="uber" />
      </div>
      <div class="logo-item tablet-only">
        <h6>Client Name</h6>
        <img src="@/assets/images/logo/dropbox.png" alt="dropbox" />
      </div>
      <div class="logo-item tablet-only">
        <h6>Client Name</h6>
        <img src="@/assets/images/logo/google.png" alt="google" />
      </div>
      <div class="logo-item desktop-only">
        <h6>Client Name</h6>
        <img src="@/assets/images/logo/uber.png" alt="uber" />
      </div>
      <div class="logo-item desktop-only">
        <h6>Client Name</h6>
        <img src="@/assets/images/logo/amazon.png" alt="amazon" />
      </div>
    </div>
    <button class="button">Try For Free</button>
  </div>
</template>

<style scoped lang="scss">
@import '@/assets/breakpoints.scss';

.partner-container {
  display: flex;
  flex-direction: column;
  align-items: center;
  text-align: center;
  gap: 4rem;
  margin-top: 10rem;

  .partner-header {
    padding: 0 2rem;
    h4 {
      span {
        display: none;
        @include media-breakpoint-up(md) {
          display: inline;
        }
      }
    }
  }

  .logo-container {
    display: grid;
    grid-template-columns: auto;
    margin-bottom: 2rem;
    gap: 2rem 0;

    @include media-breakpoint-up(md) {
      grid-template-columns: auto auto;
      gap: 0;
    }

    @include media-breakpoint-up(lg) {
      grid-template-columns: auto auto auto;
    }

    @include media-breakpoint-up(xl) {
      grid-template-columns: auto auto auto auto;
    }

    .logo-item {
      border: 1px solid #d8d8d8;
      height: 165px;
      display: flex;
      align-items: center;
      flex-direction: column;
      justify-content: center;
      padding: 0px 20px;
      width: 250px;

      @include media-breakpoint-up(md) {
        width: 220px;
        padding: 15px 20px;
      }

      &.tablet-only {
        display: none;
        @include media-breakpoint-up(md) {
          display: flex;
        }
      }

      &.desktop-only {
        display: none;
        @include media-breakpoint-up(xl) {
          display: flex;
        }
      }

      h6 {
        margin: 0;
        margin-bottom: 16px;
      }
    }
  }
}
</style>
