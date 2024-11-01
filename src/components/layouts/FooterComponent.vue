<script setup lang="ts"></script>

<template>
  <footer class="footer-container container">
    <div class="footer-start">
      <div class="footer-item">
        <h3>Pages</h3>
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
      </div>

      <div class="footer-item">
        <h3>Tomothy</h3>
        <ul class="link-list">
          <li>
            <a href="#">Eleanor Edwards</a>
          </li>
          <li>
            <a href="#">Ted Roberton</a>
          </li>
          <li>
            <a href="#">Annette Russell</a>
          </li>
          <li>
            <a href="#">Jennie Mckinney</a>
          </li>
          <li>
            <a href="#">Gloria Richards</a>
          </li>
        </ul>
      </div>

      <div class="footer-item">
        <h3>Jane Black</h3>
        <ul class="link-list">
          <li>
            <a href="#">Philip Jones</a>
          </li>
          <li>
            <a href="#">Product</a>
          </li>
          <li>
            <a href="#">Collen Russell</a>
          </li>
          <li>
            <a href="#">Marvin Hawkins</a>
          </li>
          <li>
            <a href="#">Bruce Simmons</a>
          </li>
        </ul>
      </div>
    </div>
    <div class="footer-end">
      <div class="contact-item">
        <img src="@/assets/images/icons/map.svg" alt="map-icon" />
        <h6>7480 Mockingbird Hill undefined</h6>
      </div>
      <div class="contact-item">
        <img src="@/assets/images/icons/phone.svg" alt="phone-icon" />
        <h6>(843) 555-0130</h6>
      </div>
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
    </div>
  </footer>
</template>

<style scoped lang="scss">
@import '@/assets/breakpoints.scss';
.footer-container {
  margin-top: 5rem;
  padding-top: 5rem;
  padding-bottom: 5rem;
  background-color: var(--color-background-dark);
  color: var(--color-text-light);
  a,
  h3 {
    color: var(--color-text-light);
  }

  display: flex;
  flex-direction: column;
  gap: 5rem;

  @include media-breakpoint-up(lg) {
    flex-direction: row;
    gap: 2rem;
  }

  .footer-start {
    flex: 1;
    display: flex;
    flex-direction: column;
    gap: 5rem;

    @include media-breakpoint-up(lg) {
      flex-direction: row;
    }

    @include media-breakpoint-up(xxl) {
      gap: 8rem;
    }

    .footer-item {
      text-align: center;

      .link-list {
        display: flex;
        flex-direction: column;
        gap: 20px;
      }
    }
  }

  .footer-end {
    display: flex;
    flex-direction: column;
    align-items: center;

    @include media-breakpoint-up(lg) {
      display: block;
    }

    .contact-item {
      display: flex;
      align-items: center;
      gap: 8px;
      width: 290px;
      h6 {
        margin: 0;
        margin-top: 12px;
        height: 35px;
      }
      img {
        filter: invert(100%) sepia(100%) saturate(1%) hue-rotate(300deg) brightness(200%)
          contrast(100%);
      }
    }

    .logo-list {
      margin-top: 2rem;
      display: flex;
      gap: 1rem;
    }
  }
}
</style>
