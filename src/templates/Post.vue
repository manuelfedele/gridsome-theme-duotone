<template>
  <Layout>
    <div class="post">
      <h1 class="post-title">{{ $page.post.title }}</h1>
      <div class="post-content">
        <div v-html="$page.post.content"></div>
      </div>
    </div>
  </Layout>
</template>
<script>
export default {};
</script>

<page-query>
query Post ($path: String!) {
   post: post (path: $path) {
    id
    title
    content

  }
}
</page-query>