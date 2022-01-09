<template>
    <div class="navv" style="font-family: 'Oxygen', sans-serif; ">
         <div class="flex1" >
    
      <div>
        <div class="filter shadow-sm " @click="openNav()"><i class="fas fa-bars"></i></div>
      </div>
      
   
      </div>
      <div id="mySidenav" class="sidenav shadow " >
          <div class="bc"> 
          <div class="hello">    <div ><a href="javascript:void(0)" class="closebtn" @click="closeNav()">&times;</a></div>
          <div class="closebtn2">Hello, Sign In!</div></div>
          <hr>
          <div class="container">
          <div class="shopping"><i class="far fa-user"></i>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Account</div>
          <div class="shopping"><i class="fas fa-receipt"></i>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Orders</div>
          <div class="shopping"> <i class="far fa-heart"></i>&nbsp;&nbsp;&nbsp;&nbsp;Favorite</div>
          </div>
          <hr>
       
          <div class="container  cate">
              <div class="item" v-for="cat in categories" :key="cat" @click="openNavcat()">
                  <div class="flexcat trans" v-bind:id="items.id">
                      <div  >{{cat}} </div>
                      <div ><i class="fas fa-chevron-right"></i></div>

                  </div>
                  

              </div>
          </div>
          <hr>
          <div class="flexcat container trans mb-3">
              <div ><img src="../assets/united-arab-emirates.png">&nbsp;UAE</div>
              <div><i class="fas fa-chevron-right"></i></div>

          </div>
          
          <div  class="flexcat container trans">
              <div>English</div>
              <div><i class="fas fa-chevron-right"></i></div>
          </div>
          <div class="container trans">Sell with Us</div>
          </div>
<di id="mySidenavcat" class="sidenav shadow ">
     <div class="hello">    <div ><a href="javascript:void(0)" class="closebtn" @click="closeNavcat()">&times;</a></div>
          <div class="closebtn2">Hello, Sign In!</div></div>
    Hello

</di>
          


      
      </div>
    </div>
</template>
<script>
export default {
  name: 'Nav',
  props: {
    msg: String
  },
     data(){
        return{
            categories:['Men','Women','Kids','Sports','Home','Electronics'],
            items:[
                {id:'sidenavf2'},
                {id:'sidenavf3'},
                {id:'sidenavf4'},
                {id:'sidenavf5'},
                {id:'sidenavf6'},
                {id:'sidenavf7'},
            ]
        }
    },
  methods:{
          openNav:function(){
      document.getElementById("mySidenav").style.width = "340px";
  document.getElementById("main").style.marginLeft = "250px";

     
     


    },
               openNavcat:function(){
      document.getElementById("mySidenavcat").style.width = "340px";
  document.getElementById("main").style.marginLeft = "250px";
  document.body.style.backgroundColor = "rgba(0,0,0,0.4)";
     
     


    },
        closeNav:function(){
       document.getElementById("mySidenav").style.width = "0";
  document.getElementById("main").style.marginLeft = "0";
    document.body.style.backgroundColor = "white";
    },
           closeNavcat:function(){
       document.getElementById("mySidenavcat").style.width = "0";
  document.getElementById("main").style.marginLeft = "0";
    document.body.style.backgroundColor = "white";
    },
 
  }
  
  }
</script>
<style scoped>
.sidenav {
  height: 100%; /* 100% Full-height */
  width: 0; /* 0 width - change this with JavaScript */
  position: fixed; /* Stay in place */
  z-index: 1; /* Stay on top */
  top: 0;
  left: 0;
  background-color: rgb(247, 247, 247); /* Black*/
  overflow-x: hidden; /* Disable horizontal scroll */
  padding-top: 60px; /* Place content 60px from the top */
  transition: 0.2s; /* 0.5 second transition effect to slide in the sidenav */
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
.closebtn2{
    position: absolute;
  top: 22px;
  left: 10px;
  font-size: 25px;
  margin-right: 50px;

}
.hello{
 
    color: rgb(241, 162, 14);
    font-size: 10px;
}
.shopping{
    font-size: 18px;
}
.cate{
    margin-left: 1px;
    
}
.item{
    margin-bottom: 13px;
}
.flexcat{
    display: flex;
    justify-content: space-between;
}
.bc{
    background-color: white;
    height: 550px;
}
.trans:hover{
  cursor: pointer;
  background-color: rgba(233, 158, 20, 0.719);
   animation:pulse;
  animation-duration: 2s;
  color: aliceblue;
}


</style>