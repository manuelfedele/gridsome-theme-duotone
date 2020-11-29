<template>
  <div class="posts">
    <post-on-list
      v-for="edge in $static.posts.edges"
      :key="edge.node.id"
      :post="edge.node"
    />
  </div>
</template>
<script>
import PostOnList from "./PostOnList.vue";
export default {
  components: { PostOnList },
};
</script>


<static-query>
query {
  posts: allPost {
    edges {
      node {
        id
        title
        description
        date (format: "YYYY-MM-D")
        content
        path
      }
    }
  }
}
</static-query>
