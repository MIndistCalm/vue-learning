<template>
  <div class="app">
    <post-form/>
    <post-list :posts="posts"/>
  </div>
</template>

<script>

import PostList from '@/components/PostList';
import PostForm from "@/components/PostForm";

export default {
  components:{
    PostForm, PostList
  },
  data() {
    return {
      posts: [
        { id: 1, title: "JS", body: "Описание поста" },
        { id: 2, title: "HTML", body: "Описание поста" },
        { id: 3, title: "CSS", body: "Описание поста" },
        { id: 4, title: "VUE", body: "Описание поста" },
        { id: 5, title: "REACT", body: "Описание поста" },
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
      (this.title = ""), (this.body = "");
    },
  },
};
</script>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
.app {
  padding: 20px;
}
</style>