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
        <img class="logo" src="/src/assets/images/society_logo.png" alt="logo" />
      </div>

      <div class="navbar-end">
        <ul class="logo-list">
          <li>
            <a href="#" target="_blank">
              <img src="@/assets/images/twitter.svg" alt="twitter" />
            </a>
          </li>
          <li>
            <a href="#" target="_blank">
              <img src="@/assets/images/facebook.svg" alt="facebook" />
            </a>
          </li>
          <li>
            <a href="#" target="_blank">
              <img src="@/assets/images/linkedin.svg" alt="linkedin" />
            </a>
          </li>
        </ul>
      </div>
    </div>

    <div class="header-welcome">
      <h1>The best products<br />start with Figma</h1>
      <h4>Most calendars are designed for teams. Slate is designed for freelancers</h4>
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
        display: flex;
        gap: 1.5rem;

        a {
          color: var(--color-text-light);
        }
      }
    }
    .navbar-end {
      .logo-list {
        display: flex;
        gap: 1.5rem;

        img {
          cursor: pointer;
        }
      }
    }
  }

  .header-welcome {
    margin-top: 4rem;
    text-align: center;
    padding: 0 11rem;
  }

  .header-action-button {
    width: 100%;
    display: flex;
    align-items: center;
    justify-content: center;
  }
}
</style>
