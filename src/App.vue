<template>
  <div class="app">
    <PostForm />
    <PostList :posts="posts" />
  </div>
</template>

<script>
import PostForm from "@/components/PostForm";
import PostList from "@/components/PostList";
export default {
  components: {
    PostList,
    PostForm,
  },
  data() {
    return {
      posts: [
        {
          id: 1,
          title: "javascript",
          body: "описание поста 1",
        },
        {
          id: 2,
          title: "2 javascript",
          body: "описание поста 2",
        },
        {
          id: 3,
          title: "3 javascript",
          body: "описание поста 3",
        },
        {
          id: 4,
          title: "4 javascript",
          body: "описание поста 4",
        },
      ],
      title: "",
      body: "",
    };
  },
  methods: {
    createPost() {
      const newPost = {
        id: Date.now(),
        title: this.title,
        body: this.body,
      };
      this.posts.push(newPost);
      this.title = "";
      this.body = "";
    },
  },
};
</script>

<style scoped>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

.app {
  padding: 0px 20px;
}

h4 {
  margin-bottom: 12px;
}
</style>
