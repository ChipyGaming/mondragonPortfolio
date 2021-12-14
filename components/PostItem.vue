<template>
  <div class="post-item">
    <h3>#{{ post.id }}: {{ post.title }}</h3>
    <div class="the-excerpt" v-html="post.content"></div>
  </div>
</template>

<script>
export default {
  props: {
    post: {
      type: Array,
      default: () => {}
    }
  }
};
</script>

<style scoped>
.post-item {
  box-shadow: 0 0 5px #8e43e7;
  border: 1px solid transparent;
  border-radius: 10px;
  margin: 20px 0;
  padding: 20px;
}
</style>