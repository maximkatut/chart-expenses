<script setup lang="ts">
defineProps<{
  sum: number;
}>();
</script>
<template>
  <div class="total">
    <h2 class="total-title">Total this month</h2>
    <div class="total-wrapper">
      <p class="total-sum">${{ sum }}</p>
      <div class="total-diff">
        <p class="total-percent">+2.4%</p>
        <p class="total-desc">from last month</p>
      </div>
    </div>
  </div>
</template>
