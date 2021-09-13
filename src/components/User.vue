<template>
  <div class="user">
    <span class="user-id">{{ user.id }}</span>
    <router-link 
      :to="{ path: '/userpost/' + user.id }"
    >{{ user.username }}<span>{{ user.name }}</span>
    </router-link>
    <!-- <router-link :to="{ path: '/userpost/' + user.id }">
      <nitro-btn theme="secondary"> View Post </nitro-btn>
    </router-link> -->
    <br />
    <span class="meta">
      {{ user.email }}
    </span>
  </div>
</template>

<script>
//import { NitrozenButton } from "@gofynd/nitrozen-vue";
export default {
  name: "User",
  props: ['user'],
  /* components: {
    "nitro-btn": NitrozenButton,
  }, */
};
</script>

<style lang="less" scoped>
.user {
  background-color: #fff;
  padding: 20px 30px 20px 80px;
  border-bottom: 1px solid #eee;
  position: relative;
  line-height: 20px;
  text-align: left;
  a {
    color: #34495e;
    font-weight: 600;
    text-decoration: none;
    span {
      font-size: 0.85em;
      margin-left: 10px;
      color: #828282;
    }
  }
  .user-id {
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
  .meta {
    font-size: 0.85em;
    color: #828282;
  }
}
</style>