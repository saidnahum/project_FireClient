<template>
   <div class="container mx-auto py-16 px-4 sm:px-8 lg:px-16 xl:px-20">
      <h4 class="header font-bold text-xl text-center">
         {{ cardsSection.title }}
      </h4>
      <p class="snippet text-sm text-gray-600 text-center">
         {{ cardsSection.snippet }}
      </p>
      <div class="grid lg:grid-cols-3 mt-10 justify-items-center gap-5">
         <LargeCard
            v-for="card in cardsSection.cards"
            :key="card.id"
            :card="card"
         />
      </div>
   </div>
</template>

<script>

export default {
   props: ['cardsSection']
}
</script>

<style>

</style>