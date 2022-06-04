<script setup lang="ts">
import BalanceSection from './components/BalanceSection.vue';
import ChartSection from './components/ChartSection.vue';
</script>

<template>
  <main>
    <div class="wrapper">
      <BalanceSection />
      <ChartSection />
    </div>
  </main>
</template>

<style lang="scss">
@import './styles/main.scss';
</style>
