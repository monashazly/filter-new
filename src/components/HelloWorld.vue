<template>
  <div class="hello" style="font-family: 'Oxygen', sans-serif; "  >
   
    <div class="flex1" >
         <div>
        <div class="filter shadow-sm"><i class="fas fa-sort me-1"></i>Sort</div>
      </div>
      <div>
        <div class="filter shadow-sm " @click="openNavf()"> <i class="fas fa-sort-amount-down-alt me-1"></i>Filter</div>
      </div>
      
   
      </div>
      <!-- Filter Sidenav -->
  <div id="mySidenavf" class="sidenav shadow-sm " >
  
      
    <div class="container">
      <div class="row">
        <div class="col-6">
          <h5 class="closebtn2">Filter</h5>
        </div>
        <div class="col-6"><a href="javascript:void(0)" class="closebtn" @click="closeNavf()">&times;</a></div>
      </div>
    </div>
    <hr>
   
    
      <!-- <div >
        <a href="javascript:void(0)" class="closebtn" @click="closeNav()">&times;</a></div> -->
      <div class=" mt-3 me-3">
    <div class="flex7  list"  @click="openNav2()">
      <div><div >Brands</div></div>
      <div><i class="fas fa-chevron-right"></i></div>
    </div>
    <div class="flex7 list" @click="openNav3()">
      <div>  <div >Colors</div></div>
      <div><i class="fas fa-chevron-right"></i></div>
    </div>
    <div class="flex7 list" @click="openNav4()">
      <div><div >Size</div></div>
      <div><i class="fas fa-chevron-right"></i></div>
    </div>
    <div class="flex7 list" @click="openNav5()">
      <div><div >Price</div></div>
      <div><i class="fas fa-chevron-right"></i></div>
    </div>
    </div>
    <div style="margin-top:400px" class="showResults  ">Show Results</div>
    
  
  

  
  
  
</div>
<!-- Brands Sidenav -->
<div id="mySidenav2" class="sidenav">
  <h5 class="closebtn2">Brands</h5>
 <div class="closebtn" @click="closeNav2()">&times;</div>
  <div>Brands</div>
</div>
<!-- Color Sidenav -->
<div id="mySidenav3" class="sidenav">
  <h5 class="closebtn2">Colors</h5>
  <a href="javascript:void(0)" class="closebtn" @click="closeNav3()">&times;</a>
     <div class="px-3 py-2 ">
              <div class="flex3 container ">
                <div>
                     <div class="form-check" v-for="coll in colors" :key="coll">
                  <input
                    class="form-check-input"
                    type="checkbox"
                    value=""
                    id="flexCheckDefault"
                  />
                  <label class="form-check-label" for="flexCheckDefault">
                    {{ coll }}
                  </label>
                </div>
                </div>
             <div>
                   <div v-for="coll in colors" :key="coll"
                  class="bc"
                   :style="{backgroundColor:coll}">
              
                  
                </div>
             </div>
            
              </div>
              <!-- Show Results .................. -->
              <div class="showResults mt-5">Show Results</div>
            </div>
</div>
<!-- Size sidenav -->
<div id="mySidenav4" class="sidenav">
  <h5 class="closebtn2">Size</h5>
  <a href="javascript:void(0)" class="closebtn" @click="closeNav4()">&times;</a>
  <div>
          <div class="px-3 py-2   ">
              <div class="row ms-3">
                  <div   class="col-3 mt-4 boxx shadow-sm "  v-for="box in boxes" :key="box" v-on:click="addClass" :class="isAddClass" >
                {{box}}

              </div>
              </div>
              
            <div style="margin-top:400px" class="showResults  ">Show Results</div>
              
            </div>
  </div>
</div>
<!-- Price Sidenav -->
<div id="mySidenav5" class="sidenav">
  <h5 class="closebtn2">Price</h5>
  <a href="javascript:void(0)" class="closebtn" @click="closeNav5()">&times;</a>
  <div>
            <div class="px-3 py-2">
                <div class="rangee ">
                  <div class="container  ">
                     <div >
                    <label class="mt-2" for="range-2"><b>Select Maximum Price</b></label>
                  </div>
                 
                  <input type="range" class="form-range mt-4" min="0" max="1000" step="100"  id="range-2"  v-model="value">
                
                  <div class="mt-2">Max Price : {{ value }}</div>
                  </div>
                 
    
    
    
  </div>
            </div>
            <div class="showResults ">Show Results</div>
  
</div>

      
</div>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },
    data(){
    return {
    show: false,
     value: '0',
    colors: ['red', 'blue', 'silver','purple','fuchsia','green','olive','yellow','teal','lightpink','maroon','mediumaquamarine','mediumpurple','orchid','	peru','plum','black'],
    boxes:['42','44','46','48','50','52'],
     variant: "dark",
      variants: [
        "transparent",
        "white",
        "light",
        "dark",
        "primary",
        "secondary",
        "success",
        "danger",
        "warning",
        "info",
      ],
  }},
  methods:{
    openNavf:function(){
      document.getElementById("mySidenavf").style.width = "340px";
  document.getElementById("main").style.marginLeft = "250px";

     
     


    },
       openNav2:function(){
      document.getElementById("mySidenav2").style.width = "340px";
  document.getElementById("main").style.marginLeft = "250px";
  document.body.style.backgroundColor = "rgba(0,0,0,0.4)";
     
     


    },
           openNav3:function(){
      document.getElementById("mySidenav3").style.width = "340px";
  document.getElementById("main").style.marginLeft = "250px";
  document.body.style.backgroundColor = "rgba(0,0,0,0.4)";
     
     


    },
           openNav4:function(){
      document.getElementById("mySidenav4").style.width = "340px";
  document.getElementById("main").style.marginLeft = "250px";
  document.body.style.backgroundColor = "rgba(0,0,0,0.4)";
     
     


    },
           openNav5:function(){
      document.getElementById("mySidenav5").style.width = "340px";
  document.getElementById("main").style.marginLeft = "250px";
  document.body.style.backgroundColor = "rgba(0,0,0,0.4)";
     
     


    },
    closeNavf:function(){
       document.getElementById("mySidenavf").style.width = "0";
  document.getElementById("main").style.marginLeft = "0";
    document.body.style.backgroundColor = "white";
    },
       closeNav2:function(){
       document.getElementById("mySidenav2").style.width = "0";
  document.getElementById("main").style.marginLeft = "0";
    document.body.style.backgroundColor = "white";
    },
       closeNav3:function(){
       document.getElementById("mySidenav3").style.width = "0";
  document.getElementById("main").style.marginLeft = "0";
    document.body.style.backgroundColor = "white";
    },
       closeNav4:function(){
       document.getElementById("mySidenav4").style.width = "0";
  document.getElementById("main").style.marginLeft = "0";
    document.body.style.backgroundColor = "white";
    },
       closeNav5:function(){
       document.getElementById("mySidenav5").style.width = "0";
  document.getElementById("main").style.marginLeft = "0";
    document.body.style.backgroundColor = "white";
    }
  }

}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
/* The side navigation menu */
.sidenav {
  height: 100%; /* 100% Full-height */
  width: 0; /* 0 width - change this with JavaScript */
  position: fixed; /* Stay in place */
  z-index: 1; /* Stay on top */
  top: 0;
  right: 0;
  background-color: rgb(247, 247, 247); /* Black*/
  overflow-x: hidden; /* Disable horizontal scroll */
  padding-top: 60px; /* Place content 60px from the top */
  transition: 0.5s; /* 0.5 second transition effect to slide in the sidenav */
}

/* The navigation menu links */
.sidenav a {
  padding: 8px 8px 8px 32px;
  text-decoration: none;
  font-size: 25px;
  color: #818181;
  display: inline;
  transition: 0.3s;
}

/* When you mouse over the navigation links, change their color */
.sidenav a:hover {
  color: #f1f1f1;
}

/* Position and style the close button (top right corner) */
.sidenav .closebtn {
  position: absolute;
  top: 0;
  right: 10px;
  font-size: 36px;
  margin-left: 50px;
}
.closebtn2{
    position: absolute;
  top: 22px;
  left: 10px;
  font-size: 25px;
  margin-right: 50px;

}

/* Style page content - use this if you want to push the page content to the right when you open the side navigation */
#main {
  transition: margin-left .5s;
  padding: 20px;
}

/* On smaller screens, where height is less than 450px, change the style of the sidenav (less padding and a smaller font size) */
@media screen and (max-height: 450px) {
  .sidenav {padding-top: 15px;}
  .sidenav a {font-size: 18px;}
}
.flex1 {
  display: flex;
  justify-content:center;
  margin: 20px;
  
}
.filter {
  background: white;
  color: black;
  padding: 6px 20px;
  border: 1px solid rgb(226, 217, 217);
  margin:5px;
}
.filter:hover{
  cursor: pointer;
  background-color: rgba(233, 158, 20, 0.719);
   animation:pulse;
  animation-duration: 2s;
  color: aliceblue;
}
.flex3 {
  display: flex;
  justify-content: space-between;
}
.bc{
  border:1px solid;
 
  margin: 10.5px;
  border-style: none;
  height: 15px;
  width: 15px;
}
.showResults{
  background: rgb(233, 158, 20);
  color: white;
  width: 75%;
  margin: auto;
  text-align: center;
  border:1px solid;
  border-style: none;
  border-radius: 3px;
  height: 29px;
  margin-top: 340px;
  
  

  
}
.showResults:hover{
  cursor: pointer;
  background-color: rgba(233, 158, 20, 0.719);
 
}
.boxx{
  background-color: white;
  height: 40px;
 margin :3px;
  text-align: center;
  /*  */
  border :1px solid gainsboro;
    border-radius: 4px;
  
  vertical-align: middle;
line-height: 34px;

}
.boxx:hover{
  cursor: pointer;
}
@media screen and (-webkit-min-device-pixel-ratio:0) {
    input[type='range'] {
      overflow: hidden;
      width: 250px;
      -webkit-appearance: none;
      background-color: #aaaaa7;
      height: 4px;
    }
    
    input[type='range']::-webkit-slider-runnable-track {
      height: 10px;
      -webkit-appearance: none;
      color: #13bba4;
      margin-top: -1px;
        border: none;
    border-radius: 3px;
     
    }
    
    input[type='range']::-webkit-slider-thumb {
      
      -webkit-appearance: none;
     
      cursor: pointer;
      
      box-shadow: -160px 0 0 160px #e7a221;
        border: 1px solid gray;
    height: 30px;
    width: 16px;
    border-radius: 50%;
    background: rgb(224, 221, 215);
    margin-top: -4px;
    }

}
.rangee{
  background-color: white;
  height: 500px;
}
.list{
  margin-left: 10px;
  margin-bottom: 10px;

}
.flex9{
  display: flex;
  justify-content: space-between;
}
.flex7{
  display: flex;
  justify-content: space-between;

}
.flex7:hover{
  cursor: pointer;
  background: #e7a221;
  color: aliceblue;
  
   animation:pulse;
  animation-duration: 2s;

}



</style>
