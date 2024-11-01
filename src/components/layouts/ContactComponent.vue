<script setup lang="ts"></script>

<template>
  <section class="contact-container" id="contact">
    <div class="contact-header">
      <h2>Contact Us</h2>
      <h4>
        Most calendars are designed for teams.<br /><span>Slate is designed for freelancers</span>
      </h4>
    </div>
    <div class="contact-content">
      <form @submit.prevent="console.log('Submitted')">
        <h3>Contact Us</h3>
        <input type="text" name="name" placeholder="Your Name" />
        <input type="email" name="email" placeholder="Your Email" />
        <textarea name="message" placeholder="Your Message" />
        <button type="submit">Send</button>
      </form>
      <div class="map-container">
        <div class="contact-list">
          <div>
            <img src="@/assets/images/icons/map.svg" alt="map-icon" />
            <h6>6386 Spring St undefined Anchorage, Georgia 12473 United States</h6>
          </div>
          <div>
            <img src="@/assets/images/icons/phone.svg" alt="phone-icon" />
            <h6>(843) 555-0130</h6>
          </div>
          <div>
            <img src="@/assets/images/icons/mail.svg" alt="mail-icon" />
            <h6>willie.jennings@example.com</h6>
          </div>
        </div>

        <img class="map" src="@/assets/images/map_image.png" alt="map" />

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
    </div>
  </section>
</template>

<style scoped lang="scss">
@import '@/assets/breakpoints.scss';
.contact-container {
  padding-top: 10rem;
  padding-bottom: 10rem;
  .contact-header {
    text-align: center;

    h4 {
      span {
        display: none;
        @include media-breakpoint-up(md) {
          display: inline;
        }
      }
    }
  }

  .contact-content {
    width: 100%;
    display: flex;
    align-items: stretch;
    flex-direction: column-reverse;
    gap: 4rem;
    margin-top: 5rem;

    @include media-breakpoint-up(xl) {
      align-items: flex-start;
      flex-direction: row;
    }

    form {
      flex: 1;
      border: 1px solid #d8d8d8;
      border-radius: 10px;
      box-shadow: 0 0 8px #d8d8d8;
      padding: 20px 30px;
      display: flex;
      flex-direction: column;
      gap: 2rem;

      @include media-breakpoint-up(sm) {
        margin: 0 4rem;
      }

      @include media-breakpoint-up(lg) {
        margin: 0 8rem;
      }

      @include media-breakpoint-up(xl) {
        margin: 0;
      }

      h3 {
        text-align: center;
      }

      button {
        align-self: flex-start;
      }
    }

    .map-container {
      width: 100%;
      display: flex;
      flex-direction: column-reverse;
      align-items: center;
      gap: 5rem;
      flex: 2;

      @include media-breakpoint-up(xl) {
        flex-direction: column;
        align-items: flex-start;
      }

      .contact-list {
        display: flex;
        gap: 1rem;
        flex-direction: column;

        @include media-breakpoint-up(md) {
          flex-direction: row;
          text-align: center;
          align-items: center;
        }

        div {
          flex: 1;
          display: flex;
          align-items: center;
          gap: 1rem;
          margin-bottom: 12px;

          h6 {
            margin: 0;
            @include media-breakpoint-up(md) {
              margin-top: 12px;
            }
          }

          @include media-breakpoint-up(md) {
            display: block;
          }
        }
      }

      .map {
        align-self: center;
        display: none;

        @include media-breakpoint-up(xl) {
          display: block;
        }
      }

      .logo-list {
        display: flex;
        gap: 1rem;
        img {
          filter: invert(69%) sepia(96%) saturate(5085%) hue-rotate(189deg) brightness(100%)
            contrast(95%);
        }
      }
    }
  }
}
</style>
