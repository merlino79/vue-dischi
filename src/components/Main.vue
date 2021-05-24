<template>
  <main>
     <div class="container">
       <div class="row">
         <div class="div">
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
      axios
    }
  },
 created(){
   console.log(axios);
 }


}
</script>

<style>

</style>