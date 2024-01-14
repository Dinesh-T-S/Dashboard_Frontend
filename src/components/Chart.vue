<template>
    <main>
      <div class="linechart">
        <Line :data="data" :options="options"  />
      </div>
    
    </main>
    
  </template>
  
  <script lang="ts">
  import {
    Chart as ChartJS,
    CategoryScale,
    LinearScale,
    PointElement,
    LineElement,
    Title,
    Tooltip,
    Legend
  } from 'chart.js'
  import { Line } from 'vue-chartjs'
  import * as chartConfig from './chartConfig.js'
  
  ChartJS.register(
    CategoryScale,
    LinearScale,
    PointElement,
    LineElement,
    Title,
    Tooltip,
    Legend
  )
  
  export default {
    name: 'App',
    components: {
      Line
    },
    data() {
      return chartConfig
    }
    
    
  }
  </script>
  
  <style scoped>
  
  .linechart{
    width:1040px;
    height:300px;
  }
  @media screen and (max-width: 1024px) {
    .linechart{
      width:300px;
    }
  }


  
  </style>
  