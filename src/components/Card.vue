<template>
 
    <div class="row">
     
   <img :src="card.poster" alt="">
   <p>
     {{card.title}}
   </p>
    
    
  
    
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

</style>