<template>
  <div class="post" v-for="post in posts">
    <div class=""><strong>Название: </strong>{{ post.title }}</div>
    <div class=""><strong>Описание: </strong>{{ post.body }}</div>
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
  border: 2px solid green;
  margin-bottom: 15px;
}
</style>
