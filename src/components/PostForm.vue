<template>
  <form @submit.prevent action="">
    <h4>Создание поста</h4>
    <input @input="post.title = $event.target.value" v-bind:value="post.title" type="text" placeholder="Название" />
    <input @input="post.body = $event.target.value" v-bind:value="post.body" type="text" placeholder="Описание" />
    <button class="btn">Отправить</button>
  </form>
</template>

<script>
export default {
  data() {
    return {
      post: {
        title: "",
        body: "",
      },
    };
  },
};
</script>

<style scoped>
input {
  width: 100%;
  border: 2px solid green;
  padding: 10px;
  margin-bottom: 10px;
}

form {
  display: flex;
  flex-direction: column;
}
.btn {
  align-self: flex-end;
  margin-top: 15px;
  padding: 10px;
  background: transparent;
  margin-bottom: 20px;
  cursor: pointer;
  transition: 0.2s ease;
}
.btn:hover {
  background-color: #c5c5c5;
}
</style>
