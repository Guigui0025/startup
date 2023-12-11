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
  <nav>

    
  </nav>>
  <div v-html="contenuAccueil.texte.html"></div>
</template>
