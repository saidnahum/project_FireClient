<template>
   <div>
      <!-- component -->
      <style>@import url('https://cdnjs.cloudflare.com/ajax/libs/MaterialDesign-Webfont/5.3.45/css/materialdesignicons.min.css')</style>
      <div v-if="!$fetchState.pending" class="mt-5 min-w-screen min-h-screen bg-gray-50 flex items-center justify-center py-5">
         <div class="w-full bg-white border-t border-b border-gray-200 px-5 py-16 md:py-24 text-gray-800">
            <div class="w-full max-w-6xl mx-auto">
               <div class="text-center max-w-xl mx-auto">
                     <h1 class="text-6xl md:text-7xl font-bold mb-5 text-gray-600">Testimonios <br>de los Clientes.</h1>
                     <h3 class="text-xl mb-5 font-light">Lorem ipsum dolor sit amet consectetur adipisicing elit.</h3>
                     <div class="text-center mb-10">
                        <span class="inline-block w-1 h-1 rounded-full bg-indigo-500 ml-1"></span>
                        <span class="inline-block w-3 h-1 rounded-full bg-indigo-500 ml-1"></span>
                        <span class="inline-block w-40 h-1 rounded-full bg-indigo-500"></span>
                        <span class="inline-block w-3 h-1 rounded-full bg-indigo-500 ml-1"></span>
                        <span class="inline-block w-1 h-1 rounded-full bg-indigo-500 ml-1"></span>
                     </div>
               </div>
               <div class="-mx-3 md:flex items-start">
                     <div class="px-3 md:w-1/3">
                        <TestimonialCard
                           v-for="testimonial in testimonials.results.slice(0, 2)"
                           :key="testimonial.login.uuid"
                           :testimonial="testimonial"
                        />
                     </div>
                     <div class="px-3 md:w-1/3">
                        <TestimonialCard
                           v-for="testimonial in testimonials.results.slice(2, 4)"
                           :key="testimonial.login.uuid"
                           :testimonial="testimonial"
                        />
                     </div>
                     <div class="px-3 md:w-1/3">
                        <TestimonialCard
                           v-for="testimonial in testimonials.results.slice(4, 6)"
                           :key="testimonial.login.uuid"
                           :testimonial="testimonial"
                        />
                     </div>
               </div>
            </div>
         </div>
      </div>

      <div v-else>
         Loading ...
      </div>
   </div>
</template>

<script>
export default {
   data() {
      return {
         testimonials: []
      }
   },
   async fetch(){
      this.testimonials = await fetch(
         'https://randomuser.me/api/?results=6'
      ).then(res => res.json())
   },
   // fetchDelay: 2000
}
</script>

<style>

</style>