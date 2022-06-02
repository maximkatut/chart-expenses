<script setup lang="ts">
import { ref, watchEffect } from 'vue';
import TotalSection from './TotalSection.vue';

type Day = {
  amount: number;
  day: string;
};

const MAX_HEIGHT_OF_CHART = 150;
const WEEK_DAYS = ['mon', 'tue', 'wed', 'thu', 'fri', 'sat', 'sun'];

const dayNumber = ref(new Date().getDay());
const weekDays = ref(null);
let maxValue = 0;
let sum = ref(0);

watchEffect(async () => {
  const data = await (await fetch('data.json')).json();
  const amounts = data.map((item: Day) => item.amount);
  weekDays.value = data;
  maxValue = Math.max(...amounts);
  sum.value = amounts.reduce((d: number, b: number) => d + b);
});

const getHeight = (amount: number) => {
  return (amount / maxValue) * MAX_HEIGHT_OF_CHART;
};
</script>

<template>
  <div class="chart">
    <h2 class="chart-title">Spending - Last 7 days</h2>
    <ul class="chart-list">
      <li
        v-for="{ day, amount } of weekDays"
        :key="day"
        class="chart-item"
        :style="{ height: getHeight(amount) + 'px' }"
      >
        <input :id="day" type="radio" name="weekday" />
        <label
          :for="day"
          :data-before="day"
          :data-after="amount"
          :class="day === WEEK_DAYS[dayNumber - 1] ? 'active' : ''"
        />
      </li>
    </ul>
  </div>
  <TotalSection :sum="sum" />
</template>
