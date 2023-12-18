<script setup>
const query = gql`
  query MyQuery($slug: String!) {
    blog(where: { slug: $slug }) {
      id
      titre
      texte {
        html
      }
      slug
      createdAt
      publishedAt
      updatedAt
    }
  }
`;

const blog = ref();

const route = useRoute();
const { data } = await useAsyncQuery(query, {
  slug: route.params.slug,
});

console.log(data.value);
blog.value = data.value.blog;
</script>

<template>
  <div
    v-if="blog"
    class="max-w-5xl mx-auto flex flex-col md:flex-row items-center justify-center"
  >
    <div class="space-y-8">
      <h2 class="text-3xl">{{ blog.titre }}</h2>

      <p class="text-lg" v-html="blog.texte.html"></p>
    </div>
  </div>
  <div v-else>
    <li>AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAH</li>
  </div>
</template>
