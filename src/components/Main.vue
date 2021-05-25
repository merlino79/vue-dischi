<template>
  <main>
     <div class="container">
       <div class="row ">
          <Search class="mb-5" />
         <div v-if="!loading" class=" flex-wrap   d-flex justify-content-center">

            <Card
            v-for="(card, index) in cards"
            :key="index"
            :card="card"
         
      
         />
        
        </div>
        
        <Loader v-else />
       
       </div>  
         
     
       
    
    </div>

  </main>
   

</template>

<script>
import axios from 'axios';
import Card from '@/components/Card.vue';
import Loader from '@/components/Loader.vue';
import Search from '@/components/Search.vue';



export default {
 
  name: 'Main',
  components:{
    Card,
    Loader,
    Search,
    
  },

  
  data(){
    return{
      
      axios,
       cards:[],
       loading:true,

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