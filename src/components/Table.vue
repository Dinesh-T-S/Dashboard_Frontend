<template>
  <div class="row">
  <div class="col">
    <div class="last">
                <div class="bottom_data">
                    <div class="bottom_data_navbar">
                        <ul>
                            <li class="nv">Automations</li>
                            <li class="nv">Campaigns</li>
                            <li class="nv">Segments</li>
                            <li class="nv">LastMonth</li>
                        </ul>
                    </div>

                    <div class="data2">
                        <img src="../assets/cart.jpg"  width="50px" height="50px"></img>
                        <div class="data1">
                            <h6>Abandoned Cart 7 Days</h6>
                            <p>4024 Sent | 124 Clicks</p>
                        </div>
                        <div class="data2_end">
                            <h5>$5,231</h5>
                            <p>41 Orders | $150 AOV</p>
                        </div>
                    </div>
                    <div class="data2">
                        <img src="../assets/cart.jpg" width="50px" height="50px"></img>
                        <div class="data1">
                            <h6>Abandoned Cart 15 mins</h6>
                            <p>4024 Sent | 124 Clicks</p>
                        </div>
                        <div class="data2_end">
                            <h5>$5,231</h5>
                            <p>41 Orders | $150 AOV</p>
                        </div>
                    </div>
                    <div class="data2">
                        <img src="../assets/cart.jpg" width="50px" height="50px"></img>
                        <div class="data1">
                            <h6>Abandoned Cart 4 Days</h6>
                            <p>4024 Sent | 124 Clicks</p>
                        </div>
                        <div class="data2_end">
                            <h5>$5,231</h5>
                            <p>41 Orders | $150 AOV</p>
                        </div>
                    </div>


                </div>

            </div>

  </div>
  <div class="col">
    <div class="card text-center cardgauge">
    <div class="card-body">
      <h5 class="card-title">Level 5</h5>
      <p class="card-text">+$32,050 in the last month</p>
        <div class="semi-donut-model-2 margin"
            style="--percentage : 90; --fill: #0083ff;">
            <div className="pin" />
        <img src="../assets/arrow.svg" alt="" class="arrow" />
        </div>
      <p class="card-bold">+$14,495</p>
    </div>
  </div>
  </div>
  
</div>
   
    
    
</template>

<script>

</script>

<style>
.bottom_data{
    float: left;

}
.bottom_data_navbar ul{
    display: flex;
    flex-direction: row;
    justify-content: space-around;
    list-style: none;
}
.bottom_data_navbar ul li{
    border-bottom: 2px solid white;
    border-radius: 0%;
    cursor: pointer;
}
.bottom_data_navbar ul li:hover{
    border-bottom: 2px solid rgb(52, 62, 255);
}
.nv{
  padding: 10px 50px;
    border-bottom: 1px solid black;
}
.bottom_data_navbar ul p{
    border: 1px solid black;
    border-radius: 50px;
    padding: 10px 20px;
    font-size: 16px;
}

.data1 h6{
  margin-top: -15px;
  margin-bottom: 10px;
  font-size: 18px;
}
.data2{
    display: grid;
    grid-template-columns: 100px 30% 50%;
    align-items: center;
    padding-left: 10px;
    padding-top: 15px;
}

.data2:hover{
  background-color: #e6f5ff;
  cursor: pointer;
}

.data2 h6:hover{
color: rgb(65, 65, 243);
  cursor: pointer;
}

.data2 img{
    border-radius: 50%;
    margin-top:-30px;
}

.data2 p{
    font-size: 12px;
    color: grey;
}
.data2_end{
    margin-left: 100px;
    text-align: right;
}


.cardgauge{
  width:360px;
  height: 300px;
  position: absolute;
}
.card-title{
  color:#0083ff;
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
  
  .arrow {
    position: absolute;
    width: 40px;
    z-index: 1;
    rotate: 135deg;
    bottom: 10.5px;
    left: 38.2%;
    transform-origin: right center;
    
}

.pin {
    position: absolute;
    height: 10px;
    width: 12px;
    background-color: var(--primary-color);
    border-radius: 100%;
    bottom: 10px;
    left: 50%;
    z-index: 2;
    outline: 8px solid #0083ff;
    box-shadow: 2px 2px 8px 6px rgba(0, 0, 0, 0.2);
}

  .margin{
    margin-left:12px;
  }

  @media screen and (max-width: 1024px) {

.bottom_data{
    float: left;
    width:100px;
  margin-left: 40px;

}

.bottom_data_navbar ul{
    display: flex;
    flex-direction: row;
    justify-content: space-around;
    list-style: none;
    
}



  .cardgauge{
  width:360px;
  margin-left:40px;
  position: relative;
}

  
  }

</style>
