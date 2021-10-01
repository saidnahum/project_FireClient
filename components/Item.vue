<template>
   <!-- Item -->
      <section class="mb-5 flex flex-col md:flex-row gap-11 py-4 px-5 bg-white rounded-md shadow-lg w-3/4 md:max-w-2xl items-center justify-center">
         <div class="text-indigo-500 flex flex-col justify-between w-3/4 h-3/4">
            <img :src="require(`@/assets/images/${item.image}`)" alt="" />
         </div>
         <div class="text-indigo-500">
            <h3 class="uppercase text-black text-2xl font-medium">{{ item.title }}</h3><br>
            <small class="uppercase">{{ item.snippet }}</small><br><br>
            <div class="flex gap-0.5 mt-4">
               <button 
                  id="addToCartButton" 
                  class="bg-indigo-600 hover:bg-indigo-500 focus:outline-none transition text-white uppercase px-8 py-3" 
                  @click="() => {
                     deleteItem(item.id)
                  }"
               >
                  Entregar
               </button>
               <button id="likeButton" class="bg-indigo-600 hover:bg-indigo-500 focus:outline-none transition text-white uppercase p-3">
                  <svg xmlns="http://www.w3.org/2000/svg" width="12" height="12" fill="currentColor" class="bi bi-suit-heart-fill" viewBox="0 0 16 16">
                     <path d="M4 1c2.21 0 4 1.755 4 3.92C8 2.755 9.79 1 12 1s4 1.755 4 3.92c0 3.263-3.234 4.414-7.608 9.608a.513.513 0 0 1-.784 0C3.234 9.334 0 8.183 0 4.92 0 2.755 1.79 1 4 1z"/>
                  </svg>
               </button>
            </div>
         </div>
      </section>
</template>

<script>
import { mapMutations } from 'vuex';
export default {
   props: ['item'],
   methods: {
      ...mapMutations(['deleteItem'])
   }
}
</script>