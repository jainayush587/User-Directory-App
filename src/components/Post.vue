<template>
  <div class="post-block">
    <span class="post-id">{{ post.id }}</span>
    <p>
      <span><b>Title:</b> {{ post.title }}</span>
      <span><b>Post:</b> {{ post.body }}</span>
    </p>
    <router-link :to="{ path: '/postcomments/' + post.id }">
      <span class="meta">
        comments
      </span>
    </router-link>
  </div>
</template>

<script>
export default {
  name: "Post",
  props: ["post"],
};
</script>

<style lang="less" scoped>
.post-block {
  background-color: #fff;
  padding: 20px 30px 20px 80px;
  border-bottom: 1px solid #eee;
  position: relative;
  line-height: 20px;
  text-align: left;
  p {
    display: flex;
    flex-direction: column;
  }
  a {
    text-decoration: none;
    .meta {
      font-size: 0.85em;
      margin-left: 10px;
      color: #828282;
    }
  }
  .post-id {
    color: #f60;
    font-size: 1.1em;
    font-weight: 700;
    position: absolute;
    top: 50%;
    left: 0;
    width: 80px;
    text-align: center;
    margin-top: -10px;
  }
}
</style>