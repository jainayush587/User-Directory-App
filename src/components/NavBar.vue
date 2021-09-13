<template>
    <div id="nav">
        <router-link to="/">User Directory</router-link>
        <router-link to="/about">Post</router-link>
    </div>
</template>

<script>
export default {
    name: "NavBar"
}
</script>

<style lang="less" scoped>
#nav {
  display: flex;
  flex-direction: row;
  a {
    padding: 30px;
    font-weight: bold;
    color: #2c3e50;

    &.router-link-exact-active {
      color: #42b983;
    }
  }
}
</style>