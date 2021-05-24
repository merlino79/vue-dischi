<template>
  <main>
     <div class="container">
       <div class="row">
         <div class="div"
         v-for="card in cards"
         :key="card.poster"
         >
           prova
         </div>

        
       </div>
    
    </div>

  </main>
   

</template>

<script>
import axios from 'axios';
export default {
  name: 'Main',
  data(){
    return{
      axios,
      cards:[],

    }
  },
 created(){
  // console.log(axios);
  axios.get('https://flynn.boolean.careers/exercises/api/array/music')
  .then(res =>{
    this.card = res.data;
    console.log(res.data);
  })
  .catch(err => {
    console.log(err);
  })
 },



}
</script>

<style>

</style>