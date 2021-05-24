<template>
  <main>
     <div class="container">
       <div class="row">
         <div class="div"
         v-for="(card, index) in cards"
         :key="index"
         >
          <p>
           {{card}}
            
          </p>
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
    this.card = res.data.response;
    this.cards.push(res.data.response)
    console.log(res.data.response);
  })
  .catch(err => {
    console.log(err);
  })
 },



}
</script>

<style lang="scss" scoped>
p{
  color: white;
}

</style>