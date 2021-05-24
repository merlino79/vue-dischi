<template>
 
        <div class="row">
          <div class="container-fluid">
                 <div class="col-sm-6 col-md-4 col-lg-3 mb-5">
          <img class="img-fluid mb-3 " :src="card.poster" alt="">
          <p>
            {{card.title}}
          </p>

        
         

        </div>


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

.row{
  p{
  color: white;
}
img{
  width: 100px;
  height: 100px;
  border-radius: 50%;
}
  
  
}



</style>