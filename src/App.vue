<template>
  <div id="app">
    <div id="nav">
      <router-link to="/">Hobe</router-link> |
      <router-link to="/create">Creat</router-link> |
      <router-link to="/join">joid</router-link> |
      <router-link to="/game">gabe</router-link>
    </div>
    <router-view/>
  </div>
</template>

<style lang="scss">
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
#nav {
  padding: 30px;
  a {
    font-weight: bold;
    color: #2c3e50;
    &.router-link-exact-active {
      color: #42b983;
    }
  }
}
</style>
