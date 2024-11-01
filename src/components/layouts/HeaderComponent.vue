<script setup lang="ts"></script>

<template>
  <div class="header-container container">
    <div class="navbar">
      <div class="navbar-start">
        <ul class="link-list">
          <li>
            <a href="#">Home</a>
          </li>
          <li>
            <a href="#feature">Product</a>
          </li>
          <li>
            <a href="#pricing">Pricing</a>
          </li>
          <li>
            <a href="#">About</a>
          </li>
          <li>
            <a href="#contact">Contact</a>
          </li>
        </ul>
        <img class="logo" src="@/assets/images/society_logo.png" alt="logo" />
      </div>

      <div class="navbar-end">
        <ul class="logo-list">
          <li>
            <a href="#" target="_blank">
              <img src="@/assets/images/twitter.svg" alt="facebook" />
            </a>
          </li>
          <li>
            <a href="#" target="_blank">
              <img src="@/assets/images/facebook.svg" alt="facebook" />
            </a>
          </li>
          <li>
            <a href="#" target="_blank">
              <img src="@/assets/images/linkedin.svg" alt="facebook" />
            </a>
          </li>
        </ul>
        <div class="menu">
          <img src="@/assets/images/menu.svg" alt="facebook" />
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
      @include media-breakpoint-up(md) {
        font-size: 74px;
        line-height: 84px;
        letter-spacing: 0.2px;
        font-weight: bold;
      }
    }

    h4 {
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
