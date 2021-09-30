<template>
   <div>
      <Navbar/>
      <div class="container px-4 sm:px-8 lg:px-16 xl:px-20 mx-auto mt-10"> 
         <div v-if="product">
            Adelante
         </div>
   
         <div v-else>
            pagina no encontrada
         </div>
      </div>
   </div>
</template>

<script>
export default {
   computed: {
      product(){
         return this.$store.getters.getProductById(this.$route.params.id)
      }
   }
}
</script>

<style>

</style>