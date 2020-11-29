<template>
  <Layout>
    <div class="content">
      <post-list />
      <div class="pagination"><div class="pagination__buttons"></div></div>
    </div>
  </Layout>
</template>

<script>
import PostList from "~/components/PostList.vue";
export default {
  components: { PostList },
  metaInfo: {
    title: "Hello, world!",
  },
};
</script>

<style>
</style>
