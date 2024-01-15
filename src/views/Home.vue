<template>
    <main class="home-page">

        <div className="greeting">
        <div className="greeting--left">
          <div className="profile">
            <span className="notification">5</span>
            <img
              className="faceimg"
              src="../assets/face.png"
              alt=""
            />
          </div>

          <div>
            <h1 className="welcome">Good Morning Dinesh</h1>
            <h5 className="subgreeting">
              Here are your stats for Today, 24 Aug 2020
            </h5>
          </div>
        </div>
        <div className="topbar--container">
          <button className="today">
            <i class="fa-solid fa-calendar-days icon icon--left" style="color: #74C0FC;"></i>
            Today
          </button>
          <h5 className="compare">compared to</h5>
          <button className="today">
            Previous
            <i class="fa-solid fa-caret-down icon icon--right" style="color: #74C0FC;"></i>
          </button>
        </div>
      </div>



        <br>
        <section>
            <div class="card-group cardsmall">
                <div class="card">
                    <div class="card-body">
                        <div class="container">
                            <div>
                                <h6 class="card-title">Total.Revenue</h6>
                            </div>
                            <div class="text textsmall">
                                <p class="status">+12.5%</p>
                            </div>
                        </div>
                    <h3 class="card-text">$32,621.72</h3>
                    <p class="card-text"><small class="text-muted">433 Orders</small></p>
                    </div>
                </div>
                <div class="card">
                    <div class="card-body">
                        <div class="container">
                            <div>
                                <h6 class="card-title">Subscribers</h6>
                            </div>
                            <div class="text textsmall">
                                <p class="status">+32.5%</p>
                            </div>
                        </div>
                    <h3 class="card-text">484205</h3>
                    <p class="card-text"><small class="text-muted">$56 Average Orders</small></p>
                    </div>
                </div>
                <div class="card">
                    <div class="card-body">
                        <div class="container">
                            <div>
                                <h6 class="card-title">Conversations </h6>
                            </div>
                            <div class="text textsmall">
                                <p class="danger">-3.4%</p>
                            </div>
                        </div>
                    <h3 class="card-text">552,553</h3>
                    <p class="card-text"><small class="text-muted">5min Average Response Time</small></p>
                    </div>
                </div>
                <div class="card">
                    <div class="card-body">
                        <div class="container">
                            <div>
                                <h6 class="card-title">PopupConversationRate </h6>
                            </div>
                            <div class="text textsmall " id="textsmall3">
                                <p class="status">+32.5%</p>
                            </div>
                        </div>
                    <h3 class="card-text">25%</h3>
                    <p class="card-text"><small class="text-muted">5% Sales Conversation Rate</small></p>
                    </div>
                </div>
            </div>      
        </section>
    

        <section>
                    <div class="container" id="graph">
                            <Chart></Chart>
                    </div>   
        </section>

        <br>
        <section>
            <Table></Table>

        </section>
    </main>
    
</template>

<script >
import Chart from '@/components/Chart.vue';
import Table from '@/components/Table.vue';


export default{
    components:{
        Chart,
        Table
    }
    
}



</script>

<style lang="scss" scoped>

.profile {
    position: relative;
    display: inline-block;
    margin-right: 15px;
  }
  
  .faceimg {
    height: 50px;
    width: 50px;
    border-radius: 50%;
    border: 4px solid rgba(226, 223, 229, 0.995);
  }
  
  
  .notification {
    position: absolute;
    top: 0;
    right: 0;
    background-color: var(--primary-color);
    border-radius: 50%;
    padding: 2px;
    color: white;
    font-size: 12px;
    z-index: 1;
    border: 2px solid white;
    width: 20px;
    height: 20px;
    background-color:rgb(42, 137, 246); 
    align-items: center;
    display: flex;
    justify-content: center;
  }
  
  .greeting {
    display: flex;
    justify-content: space-between;
    align-items: center;
  }
  
  .greeting--left {
    display: flex;
  }
  
  .welcome {
    font-size: 21px;
  }
  
  .subgreeting {
    font-size: 12px;
    color: var(--grey);
  }
  
  .topbar--container {
    display: flex;
    align-items: center;
    
  }
  
  .today {
    align-items: center;
    display: flex;
    border-radius: 20px;
    padding: 6px 12px;
    font-size: 14px;
    font-weight: bold;
    border: 1px solid var(--sec-gray);
    background-color: white;
  }
  
  .icon {
    color: var(--primary-color);
  }
  
  .icon--left {
    margin-right: 6px;
  }
  
  .icon--right {
    margin-left: 6px;
  }
  
  .compare {
    font-size: 11px;
    color: var(--gray);
    font-weight: normal;
    margin: 0 10px;
  }

#graph{
    align-items: center;
    padding-left: 60px;
}
.card-title{
    color: grey;
    font-size: 15px;
}

.card-text{
    color:black;
    font-weight: bold;
    font-size: 24px;
}

.card-body{
    background-color: white;
}
.text-muted{
    color: rgb(173, 171, 171);
    font-size: 15px;
    font-weight: lighter;
}
.status{
    background-color:  #99ff99;
    width:50px;
    text-align: center;
    padding: 1px;
    border-radius: 25px;
}
.danger{
    background-color:#ff8080;
    width:50px;
    text-align: center;
    padding: 1px;
    border-radius: 25px;
}

.container {
 display: grid;
 align-items: left; 
 grid-template-columns: 2fr 1.5fr 1fr;
}

.text{
    font-size: 12px;
}

#bottom{
    font-size: 14px;
    color: rgb(142, 142, 142);
}
.cardsmall{
    width: 100%;

}
.small{
 padding-left: 40em;   
}

@media screen and (max-width: 1024px) {
    
.small{
 padding-left: 0em;   
}
.cardsmall{
    margin-left: 30px;
    padding:10px;
}
.textsmall{
    margin-left: 140px;
}

#textsmall3{
    margin-left: 80px;
}
.card{
    width: 360px;
}
.col{
    padding-left: 10em;
}



}

</style>