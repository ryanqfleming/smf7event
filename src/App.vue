<script setup>
import { RouterLink, RouterView } from 'vue-router'
import HelloWorld from './components/HelloWorld.vue'
</script>

<template>
  <div class="titleHeader">SMF7 Event Calender</div> 
  <div class="forContainer" :style="{ backgroundImage: 'linear-gradient(rgb(0,0,0,0.9),rgb(0,0,0,0.9)), url(' + event.img + ')', backgroundBlendMode: 'multiply'}" v-for="event in events" >
  <div class="forChild" v-if="Date.now() < new Date(event.date)">
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
            id:'1',
            name: 'PECCY SCAVENGER HUNT - FRONT HALF',
            date: '2023-04-04',
            dateText: 'Tuesday April 4th',
            img: 'public/images/peccy.png',
            color: 'brown',
            details: 'Find a Peccy and turn it into your manager for a prize! Peccy is our internal mascot. He will be placed throughout the building during day and night shift!',
            time: 'All Day'
          },
          {
            id:'2',
            name: 'PECCY SCAVENGER HUNT - BACK HALF',
            date: '2023-04-06',
            dateText: 'Tuesday April 6th',
            img: 'public/images/peccy.png',
            color: 'brown',
            details: 'Find a Peccy and turn it into your manager for a prize! Peccy is our internal mascot. He will be placed throughout the building during day and night shift!',
            time: 'All Day'
          },
          {
            id:'3',
            name: 'PET BOARD',
            date: '2023-04-14',
            dateText: 'Monday - Friday 4/10 - 4/14',
            img: 'public/images/thepets.jpg',
            color: 'brown',
            details: 'Share your pet pics and receive a gift for your pet. Make sure when you post your pet picture to include your login ',
            time: 'All Week'
          },
          {
            id:'4',
            name: 'NATIONAL PET DAY',
            date: '2023-04-11',
            dateText: 'Tuesday 4/11',
            img: 'public/images/pets2.jfif',
            color: 'brown',
            details: 'Give your pet some extra care on National Pet Day!',
            time: 'All Week'
          },
          {
            id:'5',
            name: 'EARTH DAY',
            date: '2023-04-22',
            dateText: 'Saturday 4/22',
            img: 'public/images/earth.jfif',
            color: 'brown',
            details: 'SMF7 is putting together a volunteer event for earth day. Stay tuned for more information',
            time: 'All Day'
          },
        
          {
            id:'5',
            name: 'CINCO DE MAYO - FRONT HALF',
            date: '2023-05-02',
            dateText: 'Tuesday 5/2',
            img: 'public/images/cinco.webp',
            color: 'brown',
            details: 'Stay tuned for a Cinco De Mayo event. We are still in the planning process!',
            time: 'All Day'
          },
          {
            id:'5',
            name: 'CINCO DE MAYO - BACK HALF',
            date: '2023-05-04',
            dateText: 'Thursday 5/4',
            img: 'public/images/cinco.webp',
            color: 'brown',
            details: 'Stay tuned for a Cinco De Mayo event. We are still in the planning process!',
            time: 'All Day'
          },
          {
            id:'5',
            name: 'CINCO DE MAYO',
            date: '2023-05-04',
            dateText: 'Thursday 5/4',
            img: 'public/images/cinco.webp',
            color: 'brown',
            details: 'We might not do any events on the day itself',
            time: 'All Day'
          },
          {
            id:'5',
            name: 'MOTHERS DAY - FRONT HALF',
            date: '2023-05-09',
            dateText: 'Tuesday 5/9',
            img: 'public/images/mom.jfif',
            color: 'brown',
            details: 'For Mothers Day we will be hosting a Mothers of History trivia using kahoot',
            time: 'During Lunch for day and night shift'
          },
          {
            id:'5',
            name: 'MOTHERS DAY - BACK HALF',
            date: '2023-05-11',
            dateText: 'Thursday 5/11',
            img: 'public/images/mom.jfif',
            color: 'brown',
            details: 'For Mothers Day we will be hosting a Mothers of History trivia using kahoot',
            time: 'During Lunch for day and night shift'
          },
          {
            id:'5',
            name: 'MOTHERS DAY',
            date: '2023-05-11',
            dateText: 'Sunday 4/14',
            img: 'public/images/mom.jfif',
            color: 'brown',
            details: 'Celebrating mom\'s everywhere!',
            Time: 'All day'
          },
          {
            id:'5',
            name: 'ARIZONA TEA BAR - FRONT HALF',
            date: '2023-06-06',
            dateText: 'Tuesday 6/6',
            img: 'public/images/tea.jfif',
            color: 'brown',
            details: 'For National Tea day we will be giving out Arizona Tea!',
            time:'During lunch for day and night shift'
          },
           {
            id:'5',
            name: 'ARIZONA TEA BAR - BACK HALF',
            date: '2023-06-08',
            dateText: 'Thursday 6/8',
            img: 'public/images/tea.jfif',
            color: 'brown',
            details: 'For National Tea day we will be giving out Arizona Tea!',
            time:'During lunch for day and night shift'
          },
           {
            id:'5',
            name: 'NATIONAL ICE TEA DAY',
            date: '2023-06-10',
            dateText: 'Saturday 6/10',
            img: 'public/images/tea.jfif',
            color: 'brown',
            details: 'Drink a cold one!'
          },
          {
            id:'5',
            name: 'NATIONAL PINK DAY - FRONT HALF',
            date: '2023-06-19',
            dateText: 'Monday 6/19',
            img: 'public/images/pink.jfif',
            color: 'brown',
            details: 'Wear Pink to receive E-swag!'
          },
          {
            id:'5',
            name: 'NATIONAL PINK DAY - BACK HALF',
            date: '2023-06-23',
            dateText: 'Friday 6/23',
            img: 'public/images/pink.jfif',
            color: 'brown',
            details: 'Wear Pink to receive E-swag!'
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
    margin: 8px;
    margin-bottom: 20px;
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
