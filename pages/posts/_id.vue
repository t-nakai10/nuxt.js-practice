<template>
  <div>
    <h1>記事個別ページ {{ post.id }}</h1>
    <h2>{{ post.title }}</h2>
    <p>{{ post.body }}</p>
  </div>
</template>
<script>
export default {
  // async asyncData(context) {
  //   console.log(context);
  //   const response = await axios.get(
  //     "https://jsonplaceholder.typicode.com/posts/" + context.params.id
  //   );
  //   return {
  //     post: response.data,
  //   };
  // },
  async asyncData({ params }) {
    const { data } = await axios.get("/posts/" + params.id);
    return {
      post: data,
    };
  },
  head() {
    return {
      title: this.post.title,
    };
  },
};
</script>
