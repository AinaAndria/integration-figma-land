<script setup lang="ts">
import ContactComponent from '@/components/layouts/ContactComponent.vue';
import FeatureComponent from '@/components/layouts/FeatureComponent.vue';
import FooterComponent from '@/components/layouts/FooterComponent.vue';
import HeaderComponent from '@/components/layouts/HeaderComponent.vue';
import PartnerComponent from '@/components/layouts/PartnerComponent.vue';
import PricingComponent from '@/components/layouts/PricingComponent.vue';
import SubscribeComponent from '@/components/layouts/SubscribeComponent.vue';
import TestimonialComponent from '@/components/layouts/TestimonialComponent.vue';
import TrialComponent from '@/components/layouts/TrialComponent.vue';
</script>

<template>
  <HeaderComponent />
  <main class="main container">
    <FeatureComponent />
    <TrialComponent />
    <SubscribeComponent />
    <PartnerComponent />
    <TestimonialComponent />
    <PricingComponent />
    <ContactComponent />
    <FooterComponent />
  </main>
</template>

<style scoped lang="scss">
@import '@/assets/breakpoints.scss';
</style>
