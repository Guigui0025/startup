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
  <div>
    <TitresH2>Création de meubles stylés et recyclés</TitresH2>
    <p>
      Redonnez vie à votre intérieur avec RecyCraft : élégance durable, meubles
      uniques, et une touche artistique. Bienvenue dans le renouveau écologique.
    </p>
  </div>
  <div>
    <p>
      Découvrez l'élégance éco-chic chez RecyCraft. Plongez dans notre
      collection de produits uniques, alliant design raffiné et durabilité.
      Transformez votre espace avec des pièces qui racontent des histoires.
      Explorez la page produits pour trouver l'harmonie parfaite entre style et
      responsabilité.
    </p>
  </div>
</template>
