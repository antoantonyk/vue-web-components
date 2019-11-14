<template>
  <ul class>
    <li v-for="book in books" :key="book.id">
      <span class="title">{{ book.title }}</span> &mdash;
      <span class="author">{{ book.author }}</span>
    </li>
  </ul>
</template>

<script>
export default {
  name: "BookList",
  props: ["books"]
};
</script>

<style lang="scss" scoped>
@import "@/styles/_common.scss";
</style>
