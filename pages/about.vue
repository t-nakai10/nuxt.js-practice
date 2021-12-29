<template>
  <div>
    <h1>About ページ</h1>
  </div>
</template>
<script>
// export default {
//   head() {
//     return {
//       title: "About page",
//     };
//   },
//   data() {
//     return {
//       id: this.$route.params.id,
//       users: [
//         {
//           id: 1,
//           name: "jon",
//         },
//       ],
//     };
//   },
//   computed: {
//     user() {
//       return this.users.find((user) => user.id == this.id);
//     },
//   },
// };
export default {
  head() {
    return {
      title: "Aboutページ",
      meta: [
        {
          hid: "description",
          name: "description",
          content: "これはAboutページです。",
        },
      ],
    };
  },
};
</script>
