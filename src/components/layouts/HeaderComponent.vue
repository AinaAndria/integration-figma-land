<script setup lang="ts"></script>

<template>
  <section class="header-container container" id="home">
    <nav class="navbar">
      <div class="navbar-start">
        <ul class="link-list">
          <li>
            <a href="#home">Home</a>
          </li>
          <li>
            <a href="#feature">Product</a>
          </li>
          <li>
            <a href="#pricing">Pricing</a>
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
              <img src="@/assets/images/icons/twitter.svg" alt="twitter" />
            </a>
          </li>
          <li>
            <a href="#" target="_blank">
              <img src="@/assets/images/icons/facebook.svg" alt="facebook" />
            </a>
          </li>
          <li>
            <a href="#" target="_blank">
              <img src="@/assets/images/icons/linkedin.svg" alt="linkedin" />
            </a>
          </li>
        </ul>
        <div class="dropdown">
          <div class="dropbtn">
            <img src="@/assets/images/icons/menu.svg" alt="menu" />
          </div>
          <div class="dropdown-content">
            <a href="#home">Home</a>
            <a href="#feature">Product</a>
            <a href="#pricing">Pricing</a>
            <a href="#subscribe">About</a>
            <a href="#contact">Contact</a>
          </div>
        </div>
      </div>
    </nav>

    <div class="header-welcome">
      <h2>The best products start with Figma</h2>
      <h4>Most calendars are designed for teams. <span>Slate is designed for freelancers</span></h4>
    </div>

    <div class="header-action-button">
      <button type="button">Try For Free</button>
    </div>
  </section>
</template>

<style scoped lang="scss">
@import '@/assets/breakpoints.scss';
.header-container {
  height: 100vh;
  height: 100svh;
  min-height: 800px;
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

      .dropbtn {
        display: block;
        @include media-breakpoint-up(lg) {
          display: none;
        }

        img {
          cursor: pointer;
        }
      }

      .dropdown {
        position: relative;
        display: inline-block;

        &:hover {
          .dropdown-content {
            display: block;
          }
        }

        .dropdown-content {
          display: none;
          position: absolute;
          right: 0;
          background-color: #33333399;
          min-width: 160px;
          box-shadow: 0px 8px 16px 0px rgba(0, 0, 0, 0.2);
          z-index: 1;

          a {
            color: var(--color-text-light);
            padding: 12px 16px;
            display: block;
          }
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
