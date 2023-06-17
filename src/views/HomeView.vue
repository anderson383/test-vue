<script setup>

import BreadCrumbs from '../components/features/breadcrumbs/BreadCrumbs.vue'
import ChartsResume from '../components/features/charts-resume/ChartsResume.vue'
import ChartSelling from '../components/features/chart-selling/ChartSelling.vue'
import SalesChart from '../components/icons/charts/SalesChart.vue'
import DashGalery from '../components/features/dash-galery/DashGalery.vue'

</script>

<template>
  <main>
    <BreadCrumbs />
    <!-- <TheWelcome /> -->

    <div class="container">

      <div class="dashboard">
        <div class="column">
          <ChartSelling />
          <ChartsResume/>
        </div>
        <div class="column">
          <div class="sales-chart">
            <SalesChart />
          </div>
          <DashGalery/>
        </div>
      </div>
    </div>
    
  </main>
</template>

<style lang="scss">
  @import '../assets/modules/mixins';
  .column {
    display: flex;
    flex-direction: column;
    gap: 25px;
  }

  .sales-chart {
    @include media('mobile') {
      display: none;
    }
  }
  .dashboard {
    margin-top: 2.9em;
    display: flex;
    gap: 2em;

    @include media('mobile') {
      flex-direction: column;
    }
  }


</style>
