<template>
  <div id="app">
    <div id="nav">
      
      <router-link to="/">Home</router-link> 
      <router-link to="/contact">Contact</router-link> 
      <router-link to="/admin">Admin</router-link>
      <span class="float-right">
        <router-link to="/cart">cart (0)</router-link>
      </span>
    </div>
    <div class="container-fluid">
      <router-view />
    </div>

  </div>
</template>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

#nav {
  padding: 30px;
  max-width: 1700px;
  display: flex;
  justify-content: space-between;

  a {
    font-weight: bold;
    color: #2c3e50;
    text-decoration: none;

    &.router-link-exact-active {
      color: #42b983;
    }
  }
  
}
</style>
