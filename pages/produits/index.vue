<script setup>
const query = gql`
  query Pages {
    produits {
      description
      nom
      prix
      image {
        url
      }
      slug
    }
  }
`;

const contenuProduits = ref();
const { data } = await useAsyncQuery(query);
console.log(data.value);
contenuProduits.value = data.value.produits;
</script>

<template>
  <ul
    v-if="contenuProduits"
    class="flex flex-wrap justify-evenly items-center gap-8"
  >
    <li v-for="produit in contenuProduits" :key="produit.id">
      <NuxtLink :to="`/produits/${produit.slug}`">
        <div
          class="flex flex-col items-center mb-10 transition-transform transform hover:scale-110 duration-300 z-10"
        >
          <h2 class="text-3xl text-center mb-2">{{ produit.nom }}</h2>
          <NuxtImg
            class="shadow-2xl shadow-gradient-to-r from-blue-800 via-blue-900 to-blue-800 w-40 h-40 mx-auto"
            :src="produit.image.url"
            :alt="produit.nom"
          />
        </div>
      </NuxtLink>
    </li>
  </ul>
  <ul v-else>
    <li>AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAH</li>
  </ul>
</template>
