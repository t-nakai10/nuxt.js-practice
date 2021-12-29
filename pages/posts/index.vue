<template>
  <div>
    <h1>記事一覧</h1>
    <ul>
      <li v-for="post in posts" :key="post.id">
        <nuxt-link :to="'/post' + post.id">{{ post.title }}</nuxt-link>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  async asyncData(context) {
    const posts = await context.$axios.$get(
      "https://jsonplaceholder.typicode.com/posts/"
    );
    return { posts };
  },
  // async asyncData() {
  //   const response = await axios.get(
  //     "https://jsonplaceholder.typicode.com/posts/"
  //   );
  //   return { posts: response.data };
  // },
  // asyncData() {
  //   return axios
  //     .get("https://jsonplaceholder.typicode.com/posts/")
  //     .then((response) => {
  //       return {
  //         posts: response.data,
  //       };
  //     });
  // },
  // data() {
  //   return {
  //     posts: [],
  //   };
  // },
  // mounted() {
  //   axios
  //     .get("https://jsonplaceholder.typicode.com/posts")
  //     .then((response) => (this.posts = response.data));
  // },
};
</script>
