
<script setup>
  import PieChart from '../../icons/charts/PieChart.vue'
  import BarChart from '../../icons/charts/BarChart.vue'
  import BarChartInfo from '../../icons/charts/BarChartInfo.vue'
  import IconChevron from '../../icons/IconChevron.vue';
</script>

<template>

  <div class="chart-selling">
    <div class="header-card">
      <div class="title">
        <h3>Best Selling</h3>
      </div>
      <div class="dropdown">
        <span>This Week</span>
        <IconChevron />
      </div>
    </div>
    <div class="info-day-pcs">
      <p>Tuesday</p>
      <p>215,523 pcs</p>
    </div>
    <div class="content"> 
      <div class="pie-chart">
        <PieChart />
      </div>

      <div class="bar-chart">
        <BarChart />
        <BarChartInfo />
      </div>
    </div>


  </div>

</template>

<style lang="scss">
  @import '../../../assets/modules/mixins';
  .header-card {
    display: flex;
    justify-content: space-between;
    margin-bottom: 1.6em;

    .title h3 {
      font-size: 1.5em;
    }
    .dropdown {
      display: flex;
      align-items: center;
      gap: 11px;
      font-size: 0.8em;
      color: #B7B7B7;
    }
  }
  .chart-selling {
    padding: 2.25em;
    background-color: #2D3339;
    color: #fff;
    border-radius: 17.1608px;
    font-size: 16px;


    @include media('mobile') {
      font-size: 10.5px;
    }
    
    .content {
      justify-content: center;
      display: flex;
      gap: 2em;

      .bar-chart {
        display: flex;
        flex-direction: column;
        gap: 1.5em;

        @include media('mobile') {
          display: none;
        }
      }
    }
  }

  .info-day-pcs {
    display: flex;
    justify-content: space-between;
    margin-bottom: 2.1em;
    color: #fff;
    background-color: #20262D;
    padding: 1.2em;
    border-radius: 1em;

    @include media('mobile') {
      margin-bottom: 0em;
    }
  }

  .pie-chart {
    margin-top: -3.3em;

    @include media('mobile') {
      margin-top: -7em;
    }
  }
  
</style>
