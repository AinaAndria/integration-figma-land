<script setup lang="ts"></script>

<template>
  <div class="testimonial-container">
    <h2>Testimonials</h2>
    <div>
      <img src="@/assets/images/logo/ibm.png" alt="ibm" />
    </div>
    <h4>
      Most calendars are designed for teams. Slate is designed for freelancers who want a simple way
      to plan their schedule.
    </h4>
    <div class="avatar-container">
      <img src="@/assets/images/avatar.png" alt="avatar" />
      <div>
        <h6>Orgazine across</h6>
        <h6>Ui designer</h6>
      </div>
    </div>
    <button type="button">More Testimonials</button>
  </div>
</template>

<style scoped lang="scss">
@import '@/assets/breakpoints.scss';
.testimonial-container {
  margin-top: 12rem;
  text-align: center;
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 4rem;

  .avatar-container {
    display: flex;
    gap: 8px;

    img {
      width: 50px;
      height: 50px;
    }

    div {
      text-align: left;
      h6 {
        margin: 0;
        margin-bottom: 4px;
      }
    }
  }
}
</style>
