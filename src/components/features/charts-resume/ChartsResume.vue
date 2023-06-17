<script setup>
  import IconChevron from '../../icons/IconChevron.vue';
  import ProgressBar from '../../icons/charts/ProgressBar.vue';
  import SalesWeek from '../../icons/charts/SalesWeek.vue';
  import IncomeChart from '../../icons/charts/IncomeChart.vue';
  import PieWeekChart from '../../icons/charts/PieWeekChart.vue';
  import PieWeekChartInfo from '../../icons/charts/PieWeekChartInfo.vue';
</script>
<template>
  <div class="charts-resume">
    <div class="chart chart-bar">
      <div class="header-chart">
        <div class="title">
          <h3>Best Selling</h3>
          <p>Ticket Sold</p>
        </div>
        <div class="dropdown">
          <span>This Week</span>
          <IconChevron />
        </div>
      </div>
      <ProgressBar />
    </div>
    <div class="chart">
      <div class="header-chart">
        <div class="title">
          <h3>451,509</h3>
          <p>Sales</p>
        </div>
        <div class="dropdown">
          <span>This Week</span>
          <IconChevron />
        </div>
      </div>
      <div class="chart-img  sales-week">
        <SalesWeek />
      </div>
    </div>
    <div class="chart income-chart">
      <div class="header-chart">
        <div class="title">
          <h3>456,623</h3>
          <p>Income</p>
        </div>
        <div class="dropdown">
          <span>This Week</span>
          <IconChevron />
        </div>
      </div>
      <div class="chart-img icome-montly">
        <IncomeChart />
      </div>
    </div>
    
    <div class="chart">
      <div class="header-chart justify-end pie-header">
        <div class="dropdown">
          <span>This Week</span>
          <IconChevron />
        </div>
      </div>
      <div class="pie-chart">
        <PieWeekChart />
      </div>
      <div class="pie-info">
        <PieWeekChartInfo />
      </div>
    </div>
  </div>
</template>

<style lang="scss">
  @import '../../../assets/modules/mixins';

  .charts-resume {
    display: grid;
    grid-template-columns: repeat(2, 422px);
    gap: 2em;

    @include media('mobile') {
      grid-template-columns: repeat(1, 1fr);
    }
  }

  .chart-bar {
    display: flex;
    flex-direction: column;
    justify-content: space-between;
  }
  .chart {
    padding: 1.8em 1.8em 1em;
    box-sizing: border-box;
    background-color: #2D3339;
    border-radius: 1em;
    position: relative;
    min-height: 181px;

    &.income-chart {
      @include media('mobile') {
        display: none !important;
      }
    }

    .header-chart {
      display: flex;
      justify-content: space-between;
      align-items: flex-start;
  
      .title {
        h3 {
          color: #fff;
          font-size: 1em;
        }
        p {
          margin-top: 8px;
          color: rgba(255, 255, 255, 0.6);
        }
      }
      .dropdown {
        display: flex;
        align-items: center;
        gap: 11px;
        font-size: 14px;
        color: #B7B7B7;
      }
    }

    .sales-week {
      position: absolute;
      overflow: hidden;
      width: 100%;
      left: 4px;
      bottom: -24px;
    }

    .icome-montly {
      position: absolute;
      width: 100%;
      overflow: hidden;
      left: 0px;
      bottom: -40px;

      
    }

    


    .pie-chart {
      position: absolute;
      width: 100%;
      overflow: hidden;
      bottom: 14%;

      @include media('mobile') {
        position: static;
        margin-top: 0px;
        svg {
          width: 100% !important;
          height: 179px !important;
        }
      }
    }

    .pie-info {
      position: absolute;
      width: 100%;
      right: -16%;
      bottom: 14%;

      @include media('mobile') {
        display: none;
      }
    }

    .pie-header {
      @include media('mobile') {
        display: none;
      }
    }
  }
</style>