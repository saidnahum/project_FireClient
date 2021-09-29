<template>
   <body class="antialiased" x-data="{ isOpen : false}">
      
      <!-- hero -->
      <div class="hero bg-gray-100 py-16">
         <!-- container -->
         <div class="container px-4 sm:px-8 lg:px-16 xl:px-20 mx-auto">
            <!-- hero wrapper -->
            <div
               class="
                  hero-wrapper
                  grid grid-cols-1
                  md:grid-cols-12
                  gap-8
                  items-center
               "
            >
               <!-- hero text -->
               <div class="hero-text col-span-7 px-10">
                  <h1
                     class="
                        font-bold
                        text-4xl
                        md:text-5xl
                        max-w-xl
                        text-gray-900
                        leading-tight
                     "
                  >
                     Encuentra el Extintor Adecuado
                  </h1>
                  <hr class="w-12 h-1 bg-orange-500 rounded-full mt-8" />
                  <p
                     class="
                        text-gray-800 text-base
                        leading-relaxed
                        mt-8
                     "
                  >
                     Un incendio puede ser devastador y repercutir con muchas pérdidas y riesgo para las personas, por estas causas es importante estar prevenido para actuar contra el fuego en casas, coches o lugares donde pueda existir un riesgo de incendio, por ello es necesario que cuente con un equipo contra incendios.
                  </p>
                  <div
                     class="
                        get-app
                        flex
                        space-x-5
                        mt-10
                        justify-center
                        md:justify-start
                     "
                  >
                     <button
                        class="
                           apple
                           bg-red-500
                           text-white
                           shadow-md
                           px-3
                           py-2
                           rounded-lg
                           flex
                           items-center
                           space-x-4
                        "
                     >
                        Empezar Búsqueda
                     </button>
                  </div>
               </div>

               <!-- hero image -->
               <div class="hero-image col-span-5 px-10">
                  <img src="~/assets/svg/extintor.svg" class="w-96">
               </div>
            </div>
         </div>
      </div>
      <!-- end hero -->
   </body>
</template>

<script>

export default {

};
</script>