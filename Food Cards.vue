<script setup>
import salad from '@images/Sald.png';
import steak from '@images/Steak.png';
import fish from '@images/Fish.png';
import pasta from '@images/Pasta.png';

import 'animate.css';


const plates = reactive(
  [
  {
   id:0,
   image:salad,
   title:"Salad",
   desc:"Greens, heirloom tomatoes, avocado, walnuts, cranberries, lemon vinaigrette—a vibrant salad", 
  },
  {
   id:1,
   image:pasta,
   title:"Pasta",
   desc:"Decadent chocolates, fresh berries, Pasta medley of flavors and textures",
  },
  {
   id:2,
   image:steak,
   title:"Steak",
   desc:"Grilled ribeye with garlic mashed potatoes, vegetables, and steak sauce—a delicious and hearty meal",
  },
  {
   id:3,
   image:fish,
   title:"Fish",
   desc:"Greens, heirloom tomatoes, avocado, walnuts, cranberries, lemon vinaigrette—a vibrant salad",
  },
  {
   id:4,
   image:salad,
   title:"Salad",
   desc:"Decadent chocolates, fresh berries, almond brittle, and dainty macarons—a Pasta medley of flavors and textures",
  },
  {
   id:5,
   image:pasta,
   title:"Pasta",
   desc:"Grilled ribeye with garlic mashed potatoes, vegetables, and steak sauce—a delicious and hearty meal",
  },
  {
   id:6,
   image:steak,
   title:"Steak",
   desc:"Greens, heirloom tomatoes, avocado, walnuts, cranberries, lemon vinaigrette—a vibrant salad",
  },
  {
   id:7,
   image:fish,
   title:"Fish",
   desc:"Decadent chocolates, fresh berries, almond brittle, and dainty macarons—a Pasta medley of flavors and textures",
  },
  {
   id:8,
   image:salad,
   title:"Salad",
   desc:"Grilled ribeye with garlic mashed potatoes, vegetables, and steak sauce—a delicious and hearty meal",
  },
  {
   id:9,
   image:pasta,
   title:"Pasta",
   desc:"Greens, heirloom tomatoes, avocado, walnuts, cranberries, lemon vinaigrette—a vibrant salad",
  },
  {
   id:10,
   image:steak,
   title:"Steak",
   desc:"Decadent chocolates, fresh berries, almond brittle, and dainty macarons—a Pasta medley of flavors and textures",
  },
  {
   id:11,
   image:fish,
   title:"Fish",
   desc:"Grilled ribeye with garlic mashed potatoes, vegetables, and steak sauce—a delicious and hearty meal",
  } 
  ,
  {
   id:12,
   image:salad,
   title:"Salad",
   desc:"Greens, heirloom tomatoes, avocado, walnuts, cranberries, lemon vinaigrette—a vibrant salad",
  },
  {
   id:13,
   image:pasta,
   title:"Pasta",
   desc:"Decadent chocolates, fresh berries, almond brittle, and dainty macarons—a Pasta medley of flavors and textures",
  },
  {
   id:14,
   image:steak,
   title:"Steak",
   desc:"Grilled ribeye with garlic mashed potatoes, vegetables, and steak sauce—a delicious and hearty meal",
  } ,
  {
   id:15,
   image:fish,
   title:"Fish",
   desc:"Greens, heirloom tomatoes, avocado, walnuts, cranberries, lemon vinaigrette—a vibrant salad",
  },
  {
   id:16,
   image:salad,
   title:"Salad",
   desc:"Decadent chocolates, fresh berries, almond brittle, and dainty macarons—a Pasta medley of flavors and textures",

  },
  {
   id:17,
   image:pasta,
   title:"Pasta",
   desc:"Grilled ribeye with garlic mashed potatoes, vegetables, and steak sauce—a delicious and hearty meal",
  } 
  ,
  {
   id:18,
   image:steak,
   title:"Steak",
   desc:"Grilled ribeye with garlic mashed potatoes, vegetables, and steak sauce—a delicious and hearty meal",
  } 
  ,
  {
   id:19,
   image:fish,
   title:"Fish",
   desc:"Grilled ribeye with garlic mashed potatoes, vegetables, and steak sauce—a delicious and hearty meal",
  } 
])

</script>
<template>
  <div class="parent d-flex justify-end flex-wrap" >
    <div class="layer"></div>
  <VCol cols="6" sm="4" md="3" lg="2" v-for="plate in plates">
  <div :class="{'card-body':(plate.id%2),'card-body1':!(plate.id%2)}">
  <div :class="{'card animate__backInUp':(plate.id%2),'card1 animate__backInDown':!(plate.id%2)}">
    <div :class="{'head':(plate.id%2),'head1':!(plate.id%2)}">
      <img :src="plate.image"/>
    </div>
    <div :class="{'content':(plate.id%2),'content1':!(plate.id%2)}">
      <h1 :class="{'title':(plate.id%2),'title1':!(plate.id%2)}">
        {{plate.title}}</h1>
    <div :class="{'description':(plate.id%2),'description1':!(plate.id%2)}">
      <q>{{ plate.desc }}</q>
    </div>
    </div>
  </div> 
  </div>
  </VCol>
</div>
</template>
<style>

.parent{
  width: 100% !important;
  display: flex;
  position: relative;
  justify-content: space-around;
  align-items: center;  
  background-color: rgb(var(--v-theme-forty)) !important;
}

.parent img{
  border-radius: 50%;
  background-color: rgb(var(--v-theme-primary));
  outline: 1px solid rgb(var(--v-theme-primary));
  width: 100%;
  height: 100%;
}

.layout-wrapper.layout-blank {
  position: relative;
  flex-direction: column;
}

.layer{
  position: fixed;
  top: -100px;
  left: 0;
  width: 100%;
  height: 110%;
  z-index: 0;
background: linear-gradient(#727272, #323B42);
}

.description1
{
  text-align: center;
  margin-top: -172px;
  direction: ltr;
  font-family:cursive;
}
.description
{
  font-family:cursive;
  text-align: center;
  direction: ltr;
  transition-duration: 1s;
}

/*card*/

.card-body
{
  position: relative;
  margin-bottom: 330px;
  margin-top: 35px;
}
.card
{
  margin: 0 auto;
  transition-duration: 1s;
  margin-top: 20px;
  max-width: 200px;
  border: 4px solid rgb(var(--v-theme-primary));;
  height: 300px;
  background-color: rgb(var(--v-theme-forty));
  border-radius: 15px;
  position: absolute;
  top: -50px;
}


.head
{
  background-color: rgb(var(--v-theme-forty));
  transform: translateX(4%);
  transition-duration: 1s;
  margin: 0 auto;  
  border-radius: 50%;
  border: 4px solid rgb(var(--v-theme-primary));
  width: 210px;
  max-width: 110%;
  height: 210px;
  position: absolute;
  top: -100px;
  z-index: 10 !important;
}

.content
{
  transition-duration: 1s;
  margin-top: 155px;
  z-index: 10;
}
.title
{
  text-align: center;
  transition-duration: 1s;
  position: absolute;
  right: 30%;
  top: 110px;
}
.card-body:hover
{
  position: relative;
  .card img{
  background-color: #03aed2;
  outline: 1px solid #03aed2 !important;
  }
  .card
  {
    position: absolute;
    top: -125px;
    border: 4px solid #03aed2 !important;
        box-shadow: 1px 2px 51px 11px rgba(3, 174, 210,0.50);
  }
  .head
  {
    position: absolute;
    top: 180px;
    z-index: 10;
    border: 4px solid #03aed2;
    box-shadow: 1px 2px 51px 11px rgba(3, 174, 210,0.50);

  }
  .title
  {
   text-align: center;
    transition-duration: 1s;
    position: absolute;
    right: 30%;
    top: 5px;
  }
  .content
  {
    transition-duration: 1s;
    margin-top: 55px;
  }
}

.content1
{
  transition-duration: 1s;
  transform: rotate(180deg) ;
  margin-top: 305px;
  z-index: 10;
}

/*card1*/
.card-body1
{
  position: relative;
  margin-bottom: 35px;
  margin-top: 330px;
}

.card1{
  transform: rotate(180deg);
  transition-duration: 1s;
  margin: 0 auto;
  max-width: 200px;
  border: 4px solid rgb(var(--v-theme-primary));
  height: 300px;
  border-radius: 15px;
  background-color: rgb(var(--v-theme-forty)) !important;
  position: absolute;
  top: -400px;
}
.title1
{
  text-align: center;
  transition-duration: 1s;
  position: absolute;
  z-index: 10;
  right: 33%;
  margin-top: -40px;
}

.head1
{
  background-color: rgb(var(--v-theme-forty));
  transform: rotate(180deg);
  transform: translateX(4%);
  transition-duration: 1s;
  margin: 0 auto;  
  border-radius: 50%;
  background-color: rgb(var(--v-theme-forty));
  border: 4px solid rgb(var(--v-theme-primary));
  z-index:10 !important;
  width: 210px;
  max-width: 110%;
  position: absolute;
  top: -100px;
  height: 210px;
}

.card-body1:hover{
  position: relative;
  .card1 img {
    background-color:#03aed2;
  }
  .card1
  {
  margin: 0 auto;
  transition-duration: 1s;
  max-width: 200px;
  border: 4px solid #03aed2;
  height: 300px;
  background-color: rgb(var(--v-theme-forty)) !important;
    box-shadow: 1px 2px 51px 11px rgba(3, 174, 210,0.50);
  border-radius: 15px;
  position: absolute;
  top: -320px;
  }
  .head1
  {
  background-color: rgb(var(--v-theme-forty));
      box-shadow: 1px 2px 51px 11px rgba(3, 174, 210,0.50);

  transform: translateX(4%);
  transition-duration: 1s;
  margin: 0 auto;  
  border-radius: 50%;
  border: 4px solid #03aed2;
  width: 210px;
  max-width: 110%;
  height: 210px;
  position: absolute;
  top: 180px;
  z-index: 10 !important;
  }

  .title1
  {
  text-align: center;
  transition-duration: 1s;
  position: absolute;
  right: 33%;
  top: 0px;
  }
  .content1
  {
  transition-duration: 1s;
  margin-top: 205px;
  z-index: 10;
  }
}

#app > div > div > div > div > div > div {
  margin-top:80px;
  z-index: 10;
}
</style>
<route lang="yaml">
  meta:
    layout: blank
    action: read
    subject: Auth
    redirectIfLoggedIn: true
  </route>
