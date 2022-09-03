// for dynamic routing, we start the name with an underscore(_)
<template>
  <!-- Nuxt.js looks different but uses vue-router bts -->
  <!-- Hence, we can use all the default vue-router features -->
  <h3>Single user with id: {{ $route.params.id }}</h3>
</template>

<script>
export default {
  // In nuxt.js there are some extra properties which will be ignored by vue.js
  // One of them is validate(), with a default argument which can be named anything by the user
  // This argument is basically an object having information about route params, potential
  // query params and potential vuex store
  // (validate is the equivalent of route guard in vue.js)
  validate(data) {
    return /^\d+$/.test(data.params.id); //using regex to only allow numeric values
  },
};
</script>