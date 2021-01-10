<template>
  <div>
    <div><post-item v-for="post in posts" :key="post.id" :post="post" /></div>
    <button @click="getQuery">get data</button>
  </div>
</template>

<script>
import PostItem from "./PostItem";
import gql from "graphql-tag";

const GET_POST = gql`
  query MyQuery {
    posts {
      nodes {
        id
        date
        title
        content
      }
    }
  }
`;

export default {
  name: "PostList",
  components: {
    PostItem,
  },
  data() {
    return {
      posts: [],
    };
  },
  apollo: {
    posts: {
      query: GET_POST,
    },
  },
  mounted() {
    this.$apollo.queries.posts.refetch();
  },
  methods: {
    getQuery() {
      console.log("res ", this.posts);
    },
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
