<template>
  <div class="post on-list">
    <h1 class="post-title">{{ post.title }}</h1>
    <div class="post-meta">
      <span class="post-date">{{ post.date }}</span>
    </div>
    <span class="post-tags">#Ubuntu</span>
    <div class="post-content">
      <div v-html="post.description" />
    </div>
    <div>
      <g-link class="read-more button" :to="post.path">Read more →</g-link>
    </div>
  </div>
</template>
<script>
export default {
  props: ["post"],
};
</script>

