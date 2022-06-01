<script setup lang="ts">
import BalanceSection from './components/BalanceSection.vue'
import ChartSection from './components/ChartSection.vue'
import TotalSection from './components/TotalSection.vue'
</script>

<template>
  <div class="wrapper">
    <BalanceSection />
    <ChartSection />
    <TotalSection />
  </div>
</template>

<style lang="scss">
@import './styles/main.scss';
</style>
