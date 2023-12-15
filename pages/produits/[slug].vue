<script setup>
const query = gql`
  query MyQuery($slug: String!) {
    produit(where: { slug: $slug }) {
      id
      nom
      slug
      prix
      description
      createdAt
      publishedAt
      updatedAt
      stage
      image {
        url(
          transformation: {
            image: { resize: { fit: crop, height: 1024, width: 1024 } }
          }
        )
      }
    }
  }
`;

const produit = ref();

const route = useRoute();
const { data } = await useAsyncQuery(query, {
  slug: route.params.slug,
});

console.log(data.value);
produit.value = data.value.produit;
</script>

<template>
  <div
    v-if="produit"
    class="max-w-5xl mx-auto flex flex-col md:flex-row items-center justify-center"
  >
    <NuxtImg
      :src="produit.image.url"
      :alt="produit.nom"
      class="mb-4 md:mb-0 md:mr-4"
    />
    <div class="">
      <h2 class="text-3xl">{{ produit.nom }}</h2>
      <br />
      <p class="text-lg">{{ produit.description }}</p>
      <br />

      <a
        href="#"
        class="bg-[#E75A36] text-lg text-[#222c5f] hover:text-[#E75A36] hover:bg-[#222c5f] px-4 py-2 rounded-lg mt-8"
        >Acheter</a
      >
    </div>
  </div>
  <div v-else>
    <li>Loading...</li>
  </div>
</template>
