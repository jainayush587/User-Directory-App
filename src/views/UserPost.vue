<template>
  <div class="container">
    <h2>Posts</h2>
    <post v-for="post in userPosts" :key="post.id" :post="post"></post>
  </div>
</template>

<script>
import Post from '../components/Post.vue';
export default {
  name: "UserPost",
  components: {
    Post
  },
  props: ["id"],
  data() {
    return {
      err: "",
    };
  },
  computed: {
    userPosts() {
      return this.$store.state.userInfo.userPosts;
    },
  },
  mounted() {
    this.$store.dispatch("getPosts", this.id);
  },
};
</script>
