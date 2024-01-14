<template>
    <main class="home-page">
        <section>

        <div class="container rounded-top text-black d-flex flex-row" >
            <div class="ms-4 mt-2 d-flex flex-column" style="width: 150px;">
              <img src="../assets/face.png" class="profile"
                style="z-index: 1">
            </div>
            <div class="ms-1 " style="margin-top: 30px;">
              <h3>Good Morning Dinesh</h3>
              <p id="bottom">Here are your stats for Today, 24 Aug 2020</p>
            </div>      


        <section >                
                    <div class="small"  style="margin-top:30px;">
                        <input type="date" id="example"  v-model="value" class=" round"  placeholder="Select date" >
                        <p>Compare</p>
                        <select name="prev" id="round2"  type="dropdown" placeholder="Previous Period">
                        <option value="Previous Period">Previous Period </option>
                        <option value="2">2</option>
                        <option value="3">3</option>
                        <option value="4">4</option>
                    </select>
                </div>
                
            </section>
        </div>
    </section>



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
                                <h6 class="card-title">Conversations</h6>
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
                                <h6 class="card-title">Popup Conversation Rate</h6>
                            </div>
                            <div class="text textsmall">
                                <p class="status">+32.5%</p>
                            </div>
                        </div>
                    <h3 class="card-text">25%</h3>
                    <p class="card-text"><small class="text-muted">5% Sales Conversation Rate</small></p>
                    </div>
                </div>
            </div>      
        </section>
        <br>

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
.profile{
    width: 100px;
    height: 100px;
    border-radius: 100%;
}

.round{
    border-radius:25px;
    background-color: white;
    padding: 8px;


}

#round2{
    border-color: black;
    background-color: white;
    padding: 8px;
    border-radius:25px;

}

#graph{
    align-items: center;
    padding-left: 60px;
}
.card-title{
    color: grey;
}

.status{
    background-color:  #99ff99;
    width:60px;
    text-align: center;
    padding: 2px;
    border-radius: 25px;
}
.danger{
    background-color:#ff8080;
    width:60px;
    text-align: center;
    padding: 2px;
    border-radius: 25px;
}

.container {
 display: grid;
 align-items: center; 
 grid-template-columns: 2fr 2fr 1fr;
}

.text{
    font-size: 14px;
}

#bottom{
    font-size: 14px;
    color: rgb(142, 142, 142);
}
.cardsmall{
    width: 100%;
    padding-right:4em ;
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
    margin-left: 120px;
}
.card{
    width: 360px;
}
.col{
    padding-left: 10em;
}



}

</style>