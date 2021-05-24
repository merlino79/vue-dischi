<template>
  <main>
     <div class="container">
       <div class="row">
         <Card
         v-for="(card, index) in cards"
         :key="index"
         :card="card"
        
      
         />
        
          
         
         
        
         
         
          

      
     

        
       </div>
    
    </div>

  </main>
   

</template>

<script>
import axios from 'axios';
import Card from '@/components/Card.vue';


export default {
 
  name: 'Main',
  components:{
    Card
  },

  
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
    this.cards = res.data.response;
    
    console.log(res.data.response);
  })
  .catch(err => {
    console.log(err);
  })
 },



}
</script>

<style lang="scss" scoped>


</style>