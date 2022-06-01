<script></script>
<template>
  <div class="chart">
    <h2 class="chart-title">Spending - Last 7 days</h2>
    <ul class="chart-list">
      <li class="chart-item">
        <input id="mon" type="radio" name="weekday" />
        <label for="mon" data-before="mon" data-after="$34.55"></label>
      </li>
      <li class="chart-item">
        <input id="tue" type="radio" name="weekday" />
        <label for="tue" data-before="tue"></label>
      </li>
      <li class="chart-item">
        <input id="wed" type="radio" name="weekday" checked />
        <label for="wed" data-before="wed"></label>
      </li>
      <li class="chart-item">
        <input id="thu" type="radio" name="weekday" />
        <label for="thu" data-before="thu"> </label>
      </li>
      <li class="chart-item">
        <input id="fri" type="radio" name="weekday" />
        <label for="fri" data-before="fri"> </label>
      </li>
      <li class="chart-item">
        <input id="sat" type="radio" name="weekday" />
        <label for="sat" data-before="sat"> </label>
      </li>
      <li class="chart-item">
        <input id="sun" type="radio" name="weekday" />
        <label for="sun" data-before="sun"> </label>
      </li>
    </ul>
  </div>
</template>
