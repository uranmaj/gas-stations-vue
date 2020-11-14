<template>
  <div id="app">
    <b-navbar id="nav" vertical class="header" fixed="top">
      <router-link to="/">Domov</router-link>  |
      <router-link to="/about">O nas</router-link>
    </b-navbar>
      
    <router-view />
  </div>
</template>

<style lang="scss">

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
}

#nav {
  padding-left: 30px;
  padding-top: 30px;
  font-size: 20px;
  display: flex;
  flex-direction: column;
  align-items: flex-start;

  a {
    font-weight: bold;
    color: #2c3e50;

    &.router-link-exact-active {
      color: #42b983;
    }
  }
}
</style>
