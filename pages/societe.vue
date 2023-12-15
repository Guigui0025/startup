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