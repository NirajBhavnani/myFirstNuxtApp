// In nuxt.js there's no router config file
// we just create a folder in pages(root) and name the file as index.vue
<template>
  <div>
    <input type="text" v-model="userId" />
    <button @click="goToUser">Load User</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      userId: "",
    };
  },
  methods: {
    goToUser() {
      // navigating programmatically
      this.$router.push(`/users/${this.userId}`);
    },
  },
};
</script>