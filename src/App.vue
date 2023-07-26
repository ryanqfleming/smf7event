<script setup>
import { RouterLink, RouterView } from 'vue-router'
import HelloWorld from './components/HelloWorld.vue'
</script>

<template>
  <div class="titleHeader">SMF7 Event Calender</div> 
  <div class="forContainer" :style="{ backgroundImage: 'linear-gradient(rgb(0,0,0,0.9),rgb(0,0,0,0.9)), url(' + event.img + ')', backgroundBlendMode: 'multiply'}" v-for="event in events" >
  <div class="forChild" v-if="Date.now() <= new Date(event.date)">
    <div class="childTitle">{{ event.name }}</div>
      <div class="childBody">
      <div class="timeInfo"><span>Date:  </span> {{ event.dateText }}</div>
      <div><span>Time: </span>{{ event.time }} <br><br></div>
      <div class="eventInfo"><span>Information: </span>{{ event.details }}</div>
      <div class="artwork"><img :src= "event.img"  /></div>
    </div>
  </div>
  
  </div>

</template>
<script>
  export default{
    name: 'Event Cal',
    data() {
      return {
        events : [
          {
            id:'5',
            name: '4th of July BBQ - Front Half',
            date: '2023-07-03',
            dateText: 'Monday July 3rd',
            time: 'During lunch for day and night shifts',
            img: 'images/4th.jpeg',
            color: 'brown',
            details: 'We will be having BBQ hot dogs and games in the parking lot'
          },
          {
            id:'5',
            name: '4th of July BBQ - Back Half',
            date: '2023-07-06',
            dateText: 'Thursday July 6th',
            time: 'During lunch for day and night shifts',
            img: 'images/4th.jpeg',
            color: 'brown',
            details: 'We will be having BBQ hot dogs and games in the parking lot'
          },
          {
            id: '5',
            name: 'Hero Spirit Days',
            date: '2023-07-14',
            dateText: 'All week Monday - Friday, 7/10 - 7/14',
            img: 'images/hero.jpg',
            details: 'See either a member of HR or the the Admin who works 11AM - 7:30PM near the entrance of the building to claim your Eswag'
          },
          {
            id:'5',
            name: 'Prime Shirt Hand-out - Front Half',
            date: '2023-07-10',
            dateText: 'Monday July 10th',
            time: 'During shift change 5:30PM - 6:30PM',
            img: 'images/prime.png',
            details: 'Everyone will get 1 prime shirt! Shirts will be handed out near the entrance.'
          },
          {
            id: '5',
            name: 'Amazon fact trivia with Kahoot',
            date: '2023-07-11',
            dateText: 'Tuesday July 11',
            time: 'During lunch in the main breakroom',
            img: 'images/kahoot.jpg',
            details: 'Test your Amazon history facts and win prizes!',
          },
          {
            id: '5',
            name: 'Cool down with snowcones',
            date: '2023-07-12',
            dateText: 'Wednesday July 12 during lunch',
            time: 'During lunch for day and night shift',
            img: 'images/snowcone.jpg',
            details: 'Cool down and enjoy a snow cone'
          },
          {
            id:'5',
            name: 'Prime Shirt Hand-out - Back Half',
            date: '2023-07-13',
            dateText: 'Monday July 13th',
            time: 'During shift change 5:30PM - 6:30PM',
            img: 'images/prime.png',
            details: 'Everyone will get 1 prime shirt! Shirts will be handed out near the entrance.'
          },
          {
            id: '5',
            name: 'Amazon fact trivia with Kahoot',
            date: '2023-07-13',
            dateText: 'Tuesday July 13',
            time: 'During lunch in the main breakroom',
            img: 'images/kahoot.jpg',
            details: 'Test your Amazon history facts and win prizes!',
          },
          {
            id: '5',
            name: 'Friday popcorn!',
            date: '2023-07-14',
            dateText: 'Friday July 14th',
            time: 'During lunch in the main breakroom',
            img: 'images/popcorn.jpg',
            details: 'Enjoy some fresh popcorn during your lunch'
          },
          {
            id: '5',
            name: 'Thank you Ice cream - Front Half',
            date: '2023-07-18',
            dateText: 'Tuesday July 18th',
            time: 'During lunch',
            img: 'images/icecream.jpg',
            details: 'Enjoy a scoop of vanilla ice cream'
          },
           {
            id: '5',
            name: 'Thank you Ice cream - Back Half',
            date: '2023-07-20',
            dateText: 'Thursday July 20th',
            time: 'During lunch',
            img: 'images/icecream.jpg',
            details: 'Enjoy a scoop of vanilla ice cream'
          },
          {
            id: '5',
            name: 'Nacho Time',
            date: '2023-08-03',
            dateText: 'Thursday August 1st & 3rd',
            time: ' During Lunch',
            img: 'images/nacho.jpg',
            details: 'Nachos with hot cheese served in the main breakroom during lunch for night and day shift'
          },
          {
            id: '5',
            name: 'Back to school donation drive',
            date: '2023-08-10',
            dateText: "Tuesday 8/8 & Thursday 8/10",
            time: 'During shift change 5:30pm - 6:30PM',
            img: 'images/ben.png',
            details: 'Join us in assembling back to school kit bags for children that are unable to get supplies! Hosted by SMF7 Black Employee Network.'
          },
          {
            id: '5',
            name: 'Purple Heart Day',
            date: '2023-08-07',
            dateText: 'Monday August 7th',
            time:'All Day',
            img: 'images/heart.jfif',
            details: 'Wear purple to earn E-swag show respect for those injuried or paid the ultimate sacrifice in the line of duty. We will also have an information both so you can learn more about the Purple Heart Award'
          },
          {
            id: '5',
            name: 'Women\'s Equality Day',
            date: '2023-08-24',
            dateText: 'Tuesday August 22nd & Thursday 24th',
            time: 'Startups and breaks',
            img: 'images/women.jpg',
            details: 'Women\'s Equality Day takes place on August 26th. We will be celebrating this day on Tuesday & Thursday the same week. There will be a gift handout during start of shift. We will do a toast during lunch for Day shift and First shift for Nights' 
          },
          


        ]
      }
    }
  }
</script>

<style scoped>
  span {
    font-weight: 800;
  }
  .titleHeader {
    padding: 5px;
    margin: 0px;
    background-color: rgb(20, 78, 126);
    color: white;
    text-align: center;
    font-size: 2em;
    font-family: Arial, Helvetica, sans-serif;
    
  }
  .forContainer{
    max-width: 800px;
    margin: auto;
    border-radius: 25px;
   box-shadow: 10px 10px 34px -11px rgba(184,184,184,1); 
   background-position: bottom;
   background-repeat: no-repeat;
   overflow: scroll;
   background-size: cover;
   -ms-overflow-style: none;  /* IE and Edge */
  scrollbar-width: none;  /* Firefox */

  }
  .forContainer::-webkit-scrollbar {
  display: none;
}

  .childTitle {
    font-family: Arial, Helvetica, sans-serif;
    text-align: center;
    background-color:white;
    font-weight: 800;
    /* border-color: darkgrey; */
    /* border-width: 2px; */
    /* border-style: solid; */
    border-top-right-radius: 15px;
    border-top-left-radius: 15px;
  }
  .childBody{
    padding: 10px;
    color: white;
    font-family: Arial, Helvetica, sans-serif;
    font-weight: 500;
    height: 80vh;
  }
  .artwork{
    overflow: hidden;
    padding: 10px;
    border-radius: 5px;
  }
  .artwork>img{
    border-radius: 5px;
  }
  @media  screen and (min-width: 1000px) {
    .childBody{
      font-size: 3vw;
    }
    .childTitle{
      font-size: 4vw;
     }
     .artwork>img {
      height: 20vh;
    }
    .artwork{
      height: 20vh;
      margin:0px;
      
    }
  }
  @media screen and (max-width: 1000px){
    .childBody{
      font-size: 8vw;
    }
    .childTitle{
      font-size: 8vw;
    }
    .artwork>img {
      height: 20vh;
    }
    .artwork{
      height: 20vh;
      margin:0px;
      
    }
  }
  
</style>
