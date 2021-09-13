<template>
  <div class="container">
    <h2>Users List</h2>
    <user v-for="user in users" :key="user.id" :user="user"></user>
  </div>
</template>

<script>
import User from '../components/User.vue';
export default {
  components: { User },
  name: "Home",
  data(){
    return {
      err: "",
    };
  },
  computed: {
    users() {
      return this.$store.state.userInfo.users;
    },
  },
  mounted() {
    this.$store.dispatch("getUsers");
  },
};
</script>
