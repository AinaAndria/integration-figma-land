<script setup lang="ts"></script>

<template>
  <div class="header-container container" id="home">
    <div class="navbar">
      <div class="navbar-start">
        <ul class="link-list">
          <li>
            <a href="#home">Home</a>
          </li>
          <li>
            <a href="#feature">Product</a>
          </li>
          <li>
            <a href="#trial">Pricing</a>
          </li>
          <li>
            <a href="#subscribe">About</a>
          </li>
          <li>
            <a href="#contact">Contact</a>
          </li>
        </ul>
        <img class="logo" src="@/assets/images/logo/company.png" alt="logo" />
      </div>

      <div class="navbar-end">
        <ul class="logo-list">
          <li>
            <a href="#" target="_blank">
              <img src="@/assets/images/icons/twitter.svg" alt="facebook" />
            </a>
          </li>
          <li>
            <a href="#" target="_blank">
              <img src="@/assets/images/icons/facebook.svg" alt="facebook" />
            </a>
          </li>
          <li>
            <a href="#" target="_blank">
              <img src="@/assets/images/icons/linkedin.svg" alt="facebook" />
            </a>
          </li>
        </ul>
        <div class="menu">
          <img src="@/assets/images/icons/menu.svg" alt="facebook" />
        </div>
      </div>
    </div>

    <div class="header-welcome">
      <h2>The best products start with Figma</h2>
      <h4>Most calendars are designed for teams. <span>Slate is designed for freelancers</span></h4>
    </div>

    <div class="header-action-button">
      <button type="button">Try For Free</button>
    </div>
  </div>
</template>

<style scoped lang="scss">
@import '@/assets/breakpoints.scss';
.header-container {
  height: 100vh;
  background-image: url('@/assets/images/header_background.png');
  background-position: center bottom;
  background-repeat: no-repeat;
  background-size: cover;
  color: var(--color-text-light);

  .navbar {
    display: flex;
    justify-content: space-between;
    align-items: center;

    .navbar-start {
      display: flex;
      gap: 1.5rem;
      align-items: center;

      .link-list {
        display: none;
        gap: 1.5rem;

        @include media-breakpoint-up(lg) {
          display: flex;
        }

        a {
          color: var(--color-text-light);
        }
      }
    }

    .navbar-end {
      .logo-list {
        display: none;
        gap: 1.5rem;

        @include media-breakpoint-up(lg) {
          display: flex;
        }

        img {
          cursor: pointer;
        }
      }

      .menu {
        display: block;
        @include media-breakpoint-up(lg) {
          display: none;
        }

        img {
          cursor: pointer;
        }
      }
    }
  }

  .header-welcome {
    text-align: center;
    padding: 0 1rem;
    margin-top: 8rem;

    @include media-breakpoint-up(md) {
      margin-top: 2rem;
    }

    @include media-breakpoint-up(xl) {
      padding: 0 8rem;
    }

    h2 {
      color: var(--color-text-light);
      @include media-breakpoint-up(md) {
        font-size: 74px;
        line-height: 84px;
        letter-spacing: 0.2px;
        font-weight: bold;
      }
    }

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

  .header-action-button {
    width: 100%;
    display: flex;
    align-items: center;
    justify-content: center;
  }
}
</style>
