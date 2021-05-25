<template>
  <main>
     <div class="container">
       <div class="row ">
         <div class="v-if="!loading" flex-wrap   d-flex justify-content-center">

            <Card
            v-for="(card, index) in cards"
            :key="index"
            :card="card"
        
      
         />
         
        </div>
         <div v-esle>Loading</div>
         
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
       loading: true,

    }
  },
 created(){
  // console.log(axios);
  axios.get('https://flynn.boolean.careers/exercises/api/array/music')
  .then(res =>{
    this.cards = res.data.response;
    this.loading = false;
    
    console.log(res.data.response);
  })
  .catch(err => {
    console.log(err);
  })
 },



}
</script>

<style lang="scss" scoped>
.row{
  width: 100%;
  height: 100%;
  
 
  

}




</style>