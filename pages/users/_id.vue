<template>
  <h1>ユーザID: {{ user.name }}</h1>
</template>

<script>
export default {
  data() {
    return {
      id: this.$route.params.id,
      users: [
        {
          id: 1,
          name: "john doe",
        },
        {
          id: 2,
          name: "kevin",
        },
        {
          id: 3,
          name: "harry",
        },
      ],
    };
  },
  computed: {
    user() {
      return this.users.find((user) => user.id == this.id);
    },
  },
  created() {
    console.log(this.$route);
  },
};
</script>
