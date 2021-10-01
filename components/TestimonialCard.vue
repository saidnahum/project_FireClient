<template>
   <div class="w-full mx-auto rounded-lg bg-white border border-gray-200 p-5 text-gray-800 font-light mb-6">
      <div class="w-full flex mb-4 items-center">
            <div class="overflow-hidden rounded-full w-10 h-10 bg-gray-50 border border-gray-200">
               <img :src="`${testimonial.picture.thumbnail}`" alt="">
            </div>
            <div class="flex-grow pl-3">
               <h6 class="font-bold text-sm uppercase text-gray-600">{{ testimonial.name.first }} {{ testimonial.name.last }}</h6>
            </div>
      </div>
      <div class="w-full">
            <p class="text-sm leading-tight"><span class="text-lg leading-none italic font-bold text-gray-400 mr-1">"</span>Lorem ipsum dolor sit amet consectetur adipisicing elit. Quos sunt ratione dolor exercitationem minima quas itaque saepe quasi architecto vel! Accusantium, vero sint recusandae cum tempora nemo commodi soluta deleniti.<span class="text-lg leading-none italic font-bold text-gray-400 ml-1">"</span></p>
      </div>
   </div>
</template>

<script>
export default {
   props: ['testimonial']
}
</script>

<style>

</style>