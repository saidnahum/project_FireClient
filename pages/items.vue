<template>
   <div class="container px-4 sm:px-8 lg:px-16 xl:px-20 mx-auto py-16 flex flex-col items-center justify-center">
      <h1 class="font-bold text-3xl mb-10">Mis Extintores Rentados</h1>
      <Item
         v-for="item in myRentals"
         :key="item.id"
         :item="item"
      />
   </div>
</template>

<script>
import { mapState } from 'vuex';
export default {
   computed: {
      ...mapState(['myRentals'])
   }
}
</script>

<style>

</style>