<script setup>
const query = gql`
  query MyQuery {
    blogs {
      titre
      images {
        url
      }
      slug
    }
  }
`;

const contenuBlogs = ref();
const { data } = await useAsyncQuery(query);
console.log(data.value);
contenuBlogs.value = data.value.blogs;
</script>

<template>
  <ul
    v-if="contenuBlogs"
    class="flex flex-wrap justify-evenly items-center gap-8"
  >
    <li v-for="blog in contenuBlogs" :key="blog.id">
      <NuxtLink :to="`/blog/${blog.slug}`">
        <div
          class="flex flex-col items-center mb-10 transition-transform transform hover:scale-110 duration-300 z-10"
        >
          <h2 class="text-lg text-center mb-2">{{ blog.titre }}</h2>
          <NuxtImg
            class="shadow-2xl shadow-gradient-to-r from-blue-800 via-blue-900 to-blue-800 w-40 h-40 mx-auto"
            :src="blog.images.url"
            :alt="blog.nom"
          />
        </div>
      </NuxtLink>
    </li>
  </ul>
  <ul v-else>
    <li>AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAH</li>
  </ul>
</template>
