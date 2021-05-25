<template>

    <div>
     
         <div class="  coils col-md-5 col-sm-4 col-lg-2 ms-2">
          <img class=" mb-3 " :src="card.poster" alt="">
          <p>
            {{card.author}}
            {{card.title}}
            
          </p>

    </div>
     

      
     


     

</div>
  

 
 
   
      
        
     
         
        
         
        
  
  

 
      


        

   
     
  
    
    
  
    
   

</template>

<script>
export default {
  name: 'Card',
  props:{
    card: Object
  }

}
</script>

<style lang="scss" scoped>

.coils{
  img{
   
    height: 200px;
  


  
    
   
   
  }
   p{
  color: white;
  width: 150px;
  
  
}
  
  
  
  
  
  
}




</style>