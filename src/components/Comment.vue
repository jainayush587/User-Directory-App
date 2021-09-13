<template>
  <div class="comment-block">
    <span class="comment-id">{{ comment.id }}</span>
    <p>
      <span><b>Email:</b> {{ comment.email }}</span>
      <span><b>Comment:</b> {{ comment.body }}</span>
    </p>
  </div>
</template>

<script>
export default {
  name: "Comment",
  props: ["comment"],
}
</script>

<style lang="less" scoped>
.comment-block {
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
  .comment-id {
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