<template>
  <div class="container">
    <h2>Comments</h2>
    <comment v-for="comment in commentDetails" :key="comment.id" :comment="comment"></comment>
  </div>
</template>

<script>
import Comment from '../components/Comment.vue';
export default {
  components: { Comment },
  name: "PostComments",
  props: ["id"],
  data() {
    return {
      err: "",
    };
  },
  computed: {
    commentDetails() {
      return this.$store.state.userInfo.postComments;
    },
  },
  mounted() {
    this.$store.dispatch("getComments", this.id);
  },
};
</script>