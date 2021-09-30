<template>

<nuxt-link :to="`/productos/${card.id}`" class="lg:w-full bg-white rounded-xl overflow-hidden shadow-lg hover:shadow-xl hover:scale-105 duration-500 transform transition">
   <img class="w-full h-64 object-c" :src="require(`@/assets/images/${card.image}`)" alt="">
   <div class="p-5">
      <h1 class="text-2xl font-bold">{{ card.title }}</h1>
      <p class="mt-1 text-gray-500 font-">{{ card.snippet }}</p>
   </div>
</nuxt-link>
</template>

<script>
export default {
   props: ['card']
}
</script>