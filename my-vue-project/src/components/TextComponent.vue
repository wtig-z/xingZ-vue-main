<template>
<div class="body">
  <div class="join1">
  <div class="card" >
        <div class="card-img" id="marin"> </div>
        <div class="card-discription">
            <h2 id="visit-header"> Visit Marin County </h2>
            <h2 id="visit-state"> California </h2>
            <p> Just north of San Francisco and in driving distance of Napa, Marin is the nature part of life everyone
                has been missing. From its rolling hills, to its redwood tree forests; Marin is home to unforgettable
                hikes and panoramic views. Popular spots are Muir Woods National Monument, Mount Tamalpais State Park,
                and Bolinas Ridge. </p>
        </div>
        <button id="booknowbtn" style="
    background-color: #b9e0ff;
    border-style:none;
"> <a
                href="https://www.tripadvisor.com/Tourism-g155988-Marin_County_California-Vacations.html"> View more
                information </a> </button>
    </div>
    <div class="card" >
        <div class="card-img" id="yosemite"> </div>
        <div class="card-discription">
            <h2 id="visit-header">Visit Yosemite </h2>
            <h2 id="visit-state"> California </h2>
            <p> Yosemite is a jaw dropping National Park, hidden away in California’s Sierra Nevada mountains. It’s
                famed for its giant ancient sequoia trees and iconic vistas. After a long day hiking Bridalveil Fall, El
                Capitan, or Half Dome; you can wind down at Yosemite Village which has shops, restaurants, lodging. </p>
        </div>
        <button id="booknowbtn" style="
    background-color: #b9e0ff;
    border-style:none;
"> <a
                href="https://www.tripadvisor.com/Attraction_Review-g61000-d489919-Reviews-Yosemite_Valley-Yosemite_National_Park_California.html">
                View more information </a> </button>
    </div>
    <div class="card">
        <div class="card-img" id="sb"> </div>
        <div class="card-discription">
            <h2 id="visit-header"> Visit Santa Barbara </h2>
            <h2 id="visit-state"> California </h2>
            <p> Santa Barbara is a city on the central California coast, with the Santa Ynez Mountains as dramatic
                backdrop. Downtown, Mediterranean-style white stucco buildings with red-tile roofs reflect the city’s
                Spanish colonial heritage. Upscale boutiques and restaurants offering local wines and seasonal fare line
                State Street. </p>
        </div>
        <button id="booknowbtn" style="
    background-color: #b9e0ff;
    border-style:none;
"> <a
                href="https://www.tripadvisor.com/Tourism-g33045-Santa_Barbara_California-Vacations.html"> View more
                information </a> </button>
    </div>
  </div>
    <div class="join2">
      <div class="card" >
        <div class="card-img" id="marin"> </div>
        <div class="card-discription">
            <h2 id="visit-header"> Visit Marin County </h2>
            <h2 id="visit-state"> California </h2>
            <p> Just north of San Francisco and in driving distance of Napa, Marin is the nature part of life everyone
                has been missing. From its rolling hills, to its redwood tree forests; Marin is home to unforgettable
                hikes and panoramic views. Popular spots are Muir Woods National Monument, Mount Tamalpais State Park,
                and Bolinas Ridge. </p>
        </div>
        <button id="booknowbtn" style="
    background-color: #b9e0ff;
    border-style:none;
"> <a
                href="https://www.tripadvisor.com/Tourism-g155988-Marin_County_California-Vacations.html"> View more
                information </a> </button>
    </div>
    <div class="card" >
        <div class="card-img" id="yosemite"> </div>
        <div class="card-discription">
            <h2 id="visit-header">Visit Yosemite </h2>
            <h2 id="visit-state"> California </h2>
            <p> Yosemite is a jaw dropping National Park, hidden away in California’s Sierra Nevada mountains. It’s
                famed for its giant ancient sequoia trees and iconic vistas. After a long day hiking Bridalveil Fall, El
                Capitan, or Half Dome; you can wind down at Yosemite Village which has shops, restaurants, lodging. </p>
        </div>
        <button id="booknowbtn" style="
    background-color: #b9e0ff;
    border-style:none;
"> <a
                href="https://www.tripadvisor.com/Attraction_Review-g61000-d489919-Reviews-Yosemite_Valley-Yosemite_National_Park_California.html">
                View more information </a> </button>
    </div>
    <div class="card">
        <div class="card-img" id="sb"> </div>
        <div class="card-discription">
            <h2 id="visit-header"> Visit Santa Barbara </h2>
            <h2 id="visit-state"> California </h2>
            <p> Santa Barbara is a city on the central California coast, with the Santa Ynez Mountains as dramatic
                backdrop. Downtown, Mediterranean-style white stucco buildings with red-tile roofs reflect the city’s
                Spanish colonial heritage. Upscale boutiques and restaurants offering local wines and seasonal fare line
                State Street. </p>
        </div>
        <button id="booknowbtn" style="
    background-color: #b9e0ff;
    border-style:none;
"> <a
                href="https://www.tripadvisor.com/Tourism-g33045-Santa_Barbara_California-Vacations.html"> View more
                information </a> </button>
    </div>
  </div>
    <!-- <div class="card">
        <div class="card-img"> </div>
        <div class="card-discription">
            <h2 id="visit-header"> Visit Austin </h2>
            <h2 id="visit-state"> Texas </h2>
            <p> Austin is the state capital of Texas, an inland city bordering the Hill Country region. Home to the
                famous 6th Street bar scene, Austin is known for its eclectic live-music scene centered around country,
                blues, and rock. Its many parks and lakes are popular for hiking, biking, swimming and boating. </p>
        </div>
        <button id="booknowbtn"> <a href="https://www.tripadvisor.com/Tourism-g30196-Austin_Texas-Vacations.html"> View
                more information </a> </button>
    </div> -->

</div>
</template>

<script>
export default {
  name: 'TextComponent',  // 为你的组件命名
};



</script>
<style scoped>
.body {
  top:-340px;
   position:relative;
  width:1080px;
  display: flex;
  flex-wrap: wrap;
  justify-content: center;

  padding-top: 20px;

  
}
.join1{
  position: relative;
  top:200px;
  display: flex;
  gap:110px;
  width: 100%;
    max-width: 1200px;
    /* 设置最小宽度 */
    max-width: 1200px;
    margin:0 auto;
}
.join2{
  position: relative;
  top:200px;
  display: flex;
  gap:110px;
  width: 100%;
    max-width: 1200px;
    /* 设置最小宽度 */
    max-width: 1200px;
    margin:0 auto;

}
.card {
  margin-top: 50px;
  background: white;
  display: grid;
  grid-template-columns: 300px;
  grid-template-rows: 210px 210px 80px;
  grid-template-areas: "image" "text" "bottom";
  font-family: roboto;
  border-radius: 18px;
  box-shadow:     -1rem 0 2rem #aeadad;;
  text-align: center;
  overflow: hidden;
  transition: all 0.6s ease;
/* 
  justify-content: space-between;
  width: 30%;
  flex-wrap: wrap; */
}

.card-img {
  grid-area: image;
  background: linear-gradient(
      #fff0 0%,
      #fff0,
      70%,
      #1d1d1d 100%
    ),
    url("https://imgs.search.brave.com/4v22PiahZSXE7aJOUWOKGqaqV-eQ3Wu0dg935bwsXOA/rs:fit:860:0:0/g:ce/aHR0cHM6Ly9tZWRp/YS5pc3RvY2twaG90/by5jb20vaWQvMTM1/Nzk1NzMxMC9waG90/by9hdXN0aW4tdHgt/c2t5bGluZS5qcGc_/cz02MTJ4NjEyJnc9/MCZrPTIwJmM9dHRw/eTlhazJLcXhMcVdy/R25YRDhDQWFYdDdz/UHNBV3NYQURrTThn/Y1Vzdz0");
  background-size: cover;
}

.card-description {
  grid-area: text;
  font-family: Helvetica;
  margin-top: -10px;
}

.card-description > p {
  margin: 15px;
  margin-top: -10px;
}

.visit-header,
.visit-state {
  font-family: arial;
  text-transform: uppercase;
}

.visit-state {
  font-size: 18px;
  margin-top: -18px;
  margin-bottom: 20px;
  color: #aaa;
}

.booknowbtn {
  
  background: linear-gradient(#f2eecb, #cfb997);
  grid-area: bottom;
  border: none;
  font-size: 20px;
  color: white;
  margin-top: 30px;
}

.booknowbtn:hover {
  cursor: pointer;
  background: #51a7e1;
}

.card:hover {
  transform: translateY(-1rem);
}

/* 对于特定卡片的背景图像 */
#sb {
  background-position: bottom;
  background-image: url("https://raw.githubusercontent.com/kriskosta/siteimages/main/smallsbpic.jpg");
}

#yosemite {
  background-image: url("https://discovery.sndimg.com/content/dam/images/discovery/fullset/2022/5/18/GettyImages-1353388525.jpg.rend.hgtvcom.616.347.suffix/1652924149143.jpeg");
}

#marin {
  background-image: url("https://raw.githubusercontent.com/kriskosta/siteimages/main/smallFullSizeR.jpg");
}

a {
  text-decoration: none;
  color: rgb(12, 12, 12);
}

@media (max-width: 900px) {
  body {
    height: auto;
  }
  .card {
    width: 160px;
    height: 300px;
    font-size: 10px;
  }
  .card-img {
    background-size: cover;
    width: 160px;
    height: 110px;
    margin-bottom: 0px;
  }
  .card-description {
    margin-top: -100px;
    width: 160px;
  }
  .visit-header {
    margin: 2px;
    margin-bottom: 20px;
  }
  .visit-state {
    margin-bottom: 10px;
  }
}
</style>
