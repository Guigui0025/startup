<script setup>
const query = gql`
  query PageAccueil {
    page(where: { slug: "accueil" }) {
      titre
      slug
      texte {
        html
      }
    }
  }
`;

const contenuAccueil = ref();
const { data } = await useAsyncQuery(query);
console.log(data.value);
contenuAccueil.value = data.value.page;


</script>

<template>
  
<div class="w-full h-screen overflow-hidden relative before:block before:absolute before:bg-black before:h-full before:w-full before:top-0 before:left-0 before:z-10 before:opacity-30">
  <img src="public\img\carpentry.jpg" class="absolute top-0 left-0 min-w-full ob" alt="">
  <div id="#top" class="relative z-20 max-w-screen-lg mx-auto grid grid-cols-12 h-full items-center">
    <div class="col-span-6">
      
      <h1 class="text-white font-extrabold text-5xl mb-8">Création de meubles stylés et recyclés</h1>
      <p class="text-stone-100 text-base mb-8">
Redonnez vie à votre intérieur avec RecyCraft : élégance durable, meubles
      uniques, et une touche artistique. Bienvenue dans le renouveau écologique.      </p>
      <a href="produits" class="mt-8 text-white uppercase py-4 text-base font-light px-10 border border-white hover:bg-[#00102e] ">Nos produits</a>
    </div>
  </div>
</div>
<div class="bg-[#00102e] py-20">
  <div class="max-w-screen-lg mx-auto flex justify-between items-center">
    <div class="max-w-xl">
      <h2 class="font-black text-[#f5f5f5] text-3xl mb-4">Besoin de conseils ? Nos collaborateurs sont là pour vous !</h2>
    </div>
    <a href="contact" class="text-[#e75a36] uppercase py-3 text-base px-10 border border-[#e75a36] hover:bg-[#e75a36] hover:border-[#e75a36] hover:text-[#00102e] ">Contactez-nous</a>
  </div>
</div>
<div class="py-12 relative overflow-hidden bg-white">
  <div class="grid grid-cols-2 max-w-screen-lg mx-auto">
    <div class="w-full flex flex-col items-end pr-16">
      <h2 class="text-[#64618C] font-bold text-2xl max-w-xs text-right mb-12 mt-10"></h2>
      <div class="h-full mt-auto overflow-hidden relative">
        <img src="public\img\team.jpg" class="h-full w-full object-contain" alt="">
      </div>
    </div>

    <div class="py-20 bg-[#00102e] relative before:absolute before:h-full before:w-screen before:bg-[#00102e] before:top-0 before:left-0">
      <div class="relative z-20 pl-12">
        <h2 class="text-[#e75a36] font-black text-5xl leading-snug mb-10">Apprenez-en plus sur notre startup</h2>
        <p class="text-white text-xl mb-8">
Chez RecyCraft, où l'art et la durabilité se rencontrent. Notre équipe passionnée donne vie à des meubles uniques, alliant esthétique intemporelle et responsabilité environnementale. Explorez notre univers artisanal, découvrez notre histoire et rejoignez-nous dans notre engagement envers un style de vie durable.        </p>
        <a href="societe" class="mt-8 text-[#e75a36] uppercase py-3 text-base px-10 border border-[#e75a36] hover:bg-[#e75a36] hover:border-[#e75a36] hover:text-[#00102e]">A propos de nous</a>
      </div>
    </div>
  </div>
</div>

<div class="py-4 relative overflow-hidden bg-white">
  <div class="grid grid-cols-2 max-w-screen-lg mx-auto">
    

    <div class="py-20 pr-4 bg-[#e75a36] relative before:absolute before:h-full before:w-screen before:bg-[#e75a36] before:top-0 before:right-0">
      <div class="relative z-20 pl-12">
        <h2 class="text-[#00102e] font-black text-5xl leading-snug mb-10">Découvrez l'art d'intérieur</h2>
        <p class="text-[#00102e] text-xl mb-8">
Explorez l'univers de la décoration d'intérieur avec le blog RecyCraft. Des conseils inspirants, des idées innovantes, et un style éco-responsable vous attendent. Plongez dans la créativité et transformez votre intérieur avec nos articles uniques.</p>
        <a href="blog" class="mt-8  text-white bg-[#00102e] uppercase py-3 text-l px-10 border border-[#00102e] hover:bg-white hover:text-[#00102e]">Lisez nos articles</a>
      </div>
    </div>
    <div class="w-full flex flex-col pl-16">
      <h2 class="text-[#64618C] font-bold text-2xl max-w-xs text-left mb-12 mt-10"></h2>
      <div class="h-full mt-auto overflow-hidden relative">
        <img src="public\img\kitchen.jpg" class="h-full w-full object-contain" alt="">
      </div>
    </div>

  </div>
</div>

<div class="py-12 relative overflow-hidden bg-white">
  <div class="grid grid-cols-2 max-w-screen-lg mx-auto">
    <div class="w-full flex flex-col items-end pr-16">
      <h2 class="text-[#64618C] font-bold text-2xl max-w-xs text-right mb-12 mt-10"></h2>
      <div class="h-full mt-auto overflow-hidden relative">
        <img src="public\img\team2.jpg" class="h-full w-full object-contain" alt="">
      </div>
    </div>

    <div class="py-20 bg-[#00102e] relative before:absolute before:h-full before:w-screen before:bg-[#00102e] before:top-0 before:left-0">
      <div class="relative z-20 pl-12">
        <h2 class="text-[#e75a36] font-black text-5xl leading-snug mb-10">Notre équipe à votre service</h2>
        <p class="text-white text-xl mb-8">
Découvrez les visages derrière les créations chez RecyCraft en explorant notre page dédiée à l'équipe. Plongez dans l'univers de notre petite équipe passionnée, où chaque membre contribue à l'essence artistique et éco-responsable de RecyCraft. Rencontrez les artisans qui insufflent vie à chaque meuble, partageant une vision commune de la beauté durable. Bienvenue dans l'intimité de notre équipe, où chaque personne ajoute une touche unique à notre histoire commune.        </p>
        <a href="equipe" class="mt-8 text-[#e75a36] uppercase py-3 text-base px-10 border border-[#e75a36] hover:bg-[#e75a36] hover:border-[#e75a36] hover:text-[#00102e]">Découvrez notre équipe</a>
      </div>
    
      <a 
     
    href="#top" class="fixed bottom-4 right-4 bg-blue-500 text-white p-3 rounded-full shadow-md hover:bg-blue-600 focus:outline-none focus:ring focus:border-blue-300"
  >
     ↑ </a>
  
    </div>
  </div>
   

  
</div>
</template>
