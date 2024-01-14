<template>
  <div class="row">
  <div class="col">
    <ag-grid-vue
    class="ag-theme-quartz"
    :columnDefs="columnDefs"
    :rowData="rowData"
    :suppressMenuHide="true">
    </ag-grid-vue>
  </div>
  <div class="col ">
    <div class="card text-center cardgauge">
    <div class="card-body">
      <h5 class="card-title">Level 5</h5>
      <p class="card-text">+$32,050 in the last month</p>
        <div class="semi-donut-model-2 margin"
            style="--percentage : 90; --fill: rgb(80, 201, 253) ;">
            <i class="fa-solid fa-gauge-simple-high"></i>
        </div>
      <p class="card-bold">+$14,495</p>
    </div>
  </div>
  </div>
</div>
   
    
    
</template>

<script>
import { AgGridVue } from "ag-grid-vue3";

import "ag-grid-community/styles//ag-grid.css";
import "ag-grid-community/styles//ag-theme-quartz.css";

export default{
    name:'App',
    components:{
        AgGridVue
    },

    setup() {
    return {
      columnDefs: [
        { headerName: "Automations", field: "make" },
        { headerName: "Campaigns", field: "model" },
        { headerName: "Segments", field: "make" },
        { headerName: "Last Month", field: "price",filter: 'agTextColumnFilter', },
        
      ],
      rowData: [
        { make: "Abandoned Card 7 Days", model: "cate1", price: "$35000" },
        { make: "Abandoned Card 15 Min", model: "cate2", price: "$32000" },
        { make: "Abandoned Card 15 Min", model: "cate3", price: "$72000" },
        { make: "Abandoned Card 2 Days", model: "cate4", price: "$25000" },
        { make: "Abandoned Card 45 Min", model: "cate5", price: "$10000" },
        { make: "Abandoned Card 45 Min", model: "cate5", price: "$10000" },


      ],
    };
      

    
}}


</script>

<style>

.ag-theme-quartz {
    --ag-header-height: 30px;
    --ag-header-bottom: var(--ag-row-bottom);
    --ag-header-foreground-color:black;
    --ag-header-background-color: white;
    --ag-header-cell-hover-background-color: rgba(207, 205, 211, 0.899);
    --ag-header-cell-moving-background-color: rgb(86, 207, 241);
}
.ag-theme-quartz{
  width:805px;
  height:300px;
}

.cardgauge{
  width:400px;
  height: 300px;
  position: absolute;
}
.card-title{
  color: rgb(80, 201, 253);
  font-size: 20px;
  
}
.card-text{
  color: rgb(188, 187, 187);
  font-size: 15px;
}

.card-bold{
  color: black;
  font-size: 30px;
  font-weight: bold;
}

.semi-donut-model-2{
  width: 300px;
  height: 150px;
  position: relative;
  text-align: center;
  color: #fff;
  font-size: 45px;
  font-weight: 600;
  border-radius: 150px 150px 0 0;
  overflow: hidden;
  color: var(--fill);
  display: flex;
  align-items: flex-end;
  justify-content: center;
  box-sizing : border-box;
  
}
  .semi-donut-model-2:before, .semi-donut-model-2:after{
    content: '';
    width: 300px;
    height: 150px;
    border:50px solid var(--fill);
    border-top: none;
    position: absolute;
    transform-origin :50%  0% 0;
    border-radius: 0 0 300px 300px ;
    box-sizing : border-box;
    left: 0;
    top: 100%;
  }
  .semi-donut-model-2:before {
    border-color:rgba(0,0,0,.15);
    transform: rotate(180deg);
  }
  .semi-donut-model-2:after{
      z-index: 3;
     animation : 1s fillGraphAnimation ease-in;
    transform: rotate( calc( 1deg * ( var(--percentage) * 1.4 ) ) );
  }
  
  .margin{
    margin-left:30px;
  }

  @media screen and (max-width: 1024px) {
    .ag-theme-quartz{
  width:360px;
  margin-left: 40px;
}
  .cardgauge{
  width:360px;
  margin-left:40px;
  position: relative;
}

  
  }

</style>