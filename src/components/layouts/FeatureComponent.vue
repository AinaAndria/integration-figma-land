<script setup lang="ts"></script>

<template>
  <div class="feature-container" id="feature">
    <div class="feature-header">
      <h2>Features</h2>
      <h4>
        Most calendars are designed for teams.<br /><span>Slate is designed for freelancers</span>
      </h4>
    </div>
    <div class="feature-image">
      <img class="mobile" src="@/assets/images/video_image_mobile.png" alt="video-image-mobile" />
    </div>
    <div class="feature-items">
      <div class="feature-item">
        <img src="@/assets/images/icons/drawing.svg" alt="drawing" />
        <h3>OpenType features Variable fonts</h3>
        <p>Slate helps you see how many more days you need to work to reach your financial goal.</p>
      </div>
      <div class="feature-item">
        <img src="@/assets/images/icons/paint.svg" alt="paint" />
        <h3>Design with real data</h3>
        <p>Slate helps you see how many more days you need to work to reach your financial goal.</p>
      </div>
      <div class="feature-item">
        <img src="@/assets/images/icons/brush.svg" alt="brush" />
        <h3>Fastest way to take action</h3>
        <p>Slate helps you see how many more days you need to work to reach your financial goal.</p>
      </div>
    </div>
    <div class="feature-image">
      <img class="desktop" src="@/assets/images/video_image.png" alt="video-image" />
    </div>
  </div>
</template>

<style scoped lang="scss">
@import '@/assets/breakpoints.scss';

.feature-container {
  display: flex;
  flex-direction: column;
  align-items: center;

  .feature-header {
    text-align: center;
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

  .feature-items {
    display: flex;
    align-items: center;
    gap: 4rem;
    text-align: center;
    margin-top: 2rem;

    flex-direction: column;
    padding: 0 4rem;

    @include media-breakpoint-up(md) {
      flex-direction: row;
      align-items: baseline;
    }
  }

  .feature-image {
    margin-top: 2rem;

    img {
      width: 100%;
      cursor: pointer;
    }

    .mobile {
      @include media-breakpoint-up(lg) {
        display: none;
      }
    }

    .desktop {
      display: none;
      @include media-breakpoint-up(lg) {
        display: block;
      }
    }
  }
}
</style>
