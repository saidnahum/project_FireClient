<template>
   <div class="bg-gray-100 py-16 ">
      <div class="container px-4 sm:px-8 lg:px-16 xl:px-20 mx-auto">
         <h4 class="header font-bold text-xl text-center mb-10">
            {{ cardsSection.title }}
         </h4>
         <div class="card-container grid sm:grid-cols-2 md:grid-cols-3 lg:grid-cols-4 gap-5 mt-5">
            <SmallCard
               v-for="card in cardsSection.cards"
               :key="card.id"
               :card="card"
            />
         </div>
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