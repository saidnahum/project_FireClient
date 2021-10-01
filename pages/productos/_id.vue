<template>
   <div>
      <!-- <pre>{{ product }}</pre> -->
      <div class="container px-4 sm:px-8 lg:px-16 xl:px-20 mx-auto mt-10"> 
         <div v-if="product">
            <!-- component -->
            <style>@import url(https://cdnjs.cloudflare.com/ajax/libs/MaterialDesign-Webfont/5.3.45/css/materialdesignicons.min.css);</style>
            <div class="w-full max-w-6xl rounded bg-white shadow-xl p-10 lg:p-20 mx-auto text-gray-800 relative md:text-left">
               <div class="md:flex items-center -mx-10">
                     <div class="w-full md:w-1/2 px-10 mb-10 md:mb-0">
                        <div class="relative">
                           <img :src="require(`@/assets/images/${product.image}`)" class="w-full relative z-10" alt="">
                        </div>
                     </div>
                     <div class="w-full md:w-1/2 px-10">
                        <div class="mb-10">
                           <h1 class="font-bold uppercase text-2xl mb-5">{{ product.title }}</h1>
                           <p class="text-sm text-gray-400">{{ product.snippet }}</p><br>
                           <p class="text-sm text-justify">{{ product.description }}</p>
                        </div>
                        <div class="flex items-center justify-center">
                           <div class="inline-block align-bottom mr-0 sm:mr-5">
                                 <span class="text-2xl leading-none align-baseline">$</span>
                                 <span class="font-bold text-5xl leading-none align-baseline">59</span>
                                 <span class="text-2xl leading-none align-baseline">.99</span>
                           </div>
                           <div class="inline-block align-bottom">
                              <!-- MODAL component -->
                              <div>
                                 <div class="m-10">
                                    <!-- Modal -->
                                    <div>
                                       <!-- Button -->
                                       <button @click="showModal = !showModal" class="bg-yellow-300 opacity-75 hover:opacity-100 text-yellow-900 hover:text-gray-900 rounded-full px-3 sm:px-10 py-2 font-semibold"><i class="mdi mdi-cart -ml-2 mr-2 hidden sm:block"></i>Rentar</button>

                                       <!-- Modal Background -->
                                       <div v-show="showModal" class="fixed text-gray-500 flex items-center justify-center overflow-auto z-50 bg-black bg-opacity-40 left-0 right-0 top-0 bottom-0">
                                             <!-- Modal -->
                                             <div v-show="showModal" class="bg-white rounded-xl shadow-2xl p-6 sm:w-3/12 mx-10" >
                                                <!-- Title -->
                                                <span class="text-center font-bold block text-2xl mb-3">📅 Fecha </span>
                                                <!-- Content -->
                                                <div class="flex flex-col items-center justify-center">
                                                   <p class="mb-5">Seleccione el plazo para la renta </p>
                                                   <div class="">
                                                      <vc-date-picker
                                                         :value="null"
                                                         color="indigo"
                                                         is-dark
                                                         is-range
                                                      />
                                                   </div>
                                                </div>

                                                <!-- Buttons -->
                                                <div class="text-right space-x-5 mt-5 flex items-center justify-center">
                                                   <button @click="showModal = !showModal" class="px-4 py-2 text-sm bg-red-500 text-white rounded-xl border transition-colors duration-150 ease-linear border-gray-200 focus:outline-none focus:ring-0 font-bold hover:bg-red-800 focus:bg-indigo-50 focus:text-indigo">Cancel</button>
                                                   <button 
                                                      class="bg-yellow-300 opacity-75 hover:opacity-100 text-yellow-900 hover:text-gray-900 rounded-full px-10 py-2 font-semibold"
                                                      @click="() => {
                                                         addItem(product.id)
                                                         hideModal()
                                                      }"
                                                   >
                                                      <i class="mdi mdi-cart -ml-2 mr-2"></i>Rentar Ahora
                                                   </button>
                                                </div>
                                             </div>
                                       </div>
                                    </div>

                                 </div>
                              </div>
                           </div>
                        </div>
                     </div>
               </div>
            </div>

            <Testimonial/>

         </div>
   
         <div v-else>
            <PageNotFound/>
         </div>
      </div>
   </div>
</template>

<script>
import { mapMutations } from 'vuex';
export default {
   data() {
      return {
         showModal: false
      }
   },
   computed: {
      product(){
         return this.$store.getters.getProductById(this.$route.params.id)
      }
   },
   methods: {
      ...mapMutations(['addItem']),
      hideModal(){
         this.showModal = false
      }
   }
}
</script>

<style>

</style>