<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png" />
    <h1>Food Shop</h1>
    <Products/>
  </div>
</template>

<script>
// @ is an alias to /src

import Products from '@/views/Products.vue'
export default {
  name: "Home",
  components: {
    Products

  },
};
</script>


