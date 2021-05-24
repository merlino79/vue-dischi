<template>
 
    <div class="row">
      <div class="container">
        <div class="col-sm-6 col-md-3">
          <img class="img-fluid mb-3" :src="card.poster" alt="">
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
p{
  color: white;
}

</style>