<template lang="">
    <!-- Отображение постов -->
    <div class="post" v-for="post in posts" :key="post.id">
      <div><strong>Название:</strong> {{ post.title }}</div>
      <div><strong>Описание:</strong> {{ post.body }}</div>
    </div>
</template>
<script>
export default {
  props: {
    posts: {
      type: Array,
      required: true,
    },
  },
};
</script>
<style scoped>
.post {
  padding: 15px;
  border: 1px solid black;
  margin-top: 15px;
}
</style>