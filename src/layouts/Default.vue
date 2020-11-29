<template>
  <div class="container center headings--one-size">
    <header class="header">
      <div class="header__inner">
        <div class="header__logo">
          <g-link class="logo" to="/">{{ $static.metadata.siteName }}</g-link>
        </div>
      </div>
    </header>
    <slot />
  </div>
</template>

<script>
import Prism from "prismjs";

export default {
  mounted() {
    Prism.highlightAll();
  },
};
</script>

<static-query>
query {
  metadata {
    siteName
  }
}
</static-query>
