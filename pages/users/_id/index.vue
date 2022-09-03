// for dynamic routing, we start the name with an underscore(_)
<template>
  <!-- Nuxt.js looks different but uses vue-router bts -->
  <!-- Hence, we can use all the default vue-router features -->
  <h3>Single user with id: {{ $route.params.id }}</h3>
</template>