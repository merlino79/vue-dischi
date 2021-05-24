<template>
  <div id="app">
    <div class="row">
    <Header />
    <Main />
    <Card />

    </div>
   
   

  
   
    
    
  </div>
</template>

<script>
import Header from '@/components/Header.vue'
import Main from '@/components/Main.vue'
import Card from '@/components/Card.vue'



export default {
  name: 'App',
  components: {
    Header,
    Main,
    Card,
   
  }
}
</script>

<style lang="scss">
@import '@/assets/styles/general.scss'

</style>
