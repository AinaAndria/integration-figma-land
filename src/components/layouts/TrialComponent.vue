<script setup lang="ts"></script>

<template>
  <div class="trial-container" id="trial">
    <div class="trial-start">
      <div>
        <h2>Fastest way to organize</h2>
        <h4>
          Most calendars are designed for teams.<br /><span>Slate is designed for freelancers</span>
        </h4>
      </div>
      <button type="button">Try For Free</button>
    </div>
    <div class="trial-end">
      <img src="@/assets/images/macbook.png" alt="macbook" />
    </div>
  </div>
</template>

<style scoped lang="scss">
@import '@/assets/breakpoints.scss';

.trial-container {
  margin-top: 10rem;
  display: flex;
  flex-direction: column;
  text-align: center;
  align-items: center;
  justify-content: space-between;
  gap: 2rem;

  @include media-breakpoint-up(lg) {
    text-align: left;
    flex-direction: row;
    align-items: stretch;
  }

  .trial-start {
    flex: 1;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: space-between;
    padding-bottom: 1rem;

    @include media-breakpoint-up(lg) {
      align-items: flex-start;
    }

    h2 {
      margin: 0;
    }

    h4 {
      span {
        display: none;

        @include media-breakpoint-up(md) {
          display: inline;
        }
      }
    }

    button {
      margin-top: 3rem;

      @include media-breakpoint-up(lg) {
        margin-top: 0;
      }
    }
  }

  .trial-end {
    flex: 1;
    img {
      width: 100%;
    }
  }
}
</style>
