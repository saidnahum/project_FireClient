<template>
   <div>
      <nuxt-link :to="`/productos/${card.id}`">
         <img class="w-96 h-48 rounded-lg object-cover hover:shadow-xl hover:scale-105 duration-500 transform transition" :src="require(`@/assets/images/${card.image}`)" alt="">
      </nuxt-link>
   </div>
</template>

<script>
export default {
   props: ['card']
}
</script>

<style>

</style>