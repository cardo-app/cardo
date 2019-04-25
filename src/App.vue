<template>
  <div id="app">
    <div id="nav">
      <router-link to="/">Hobe</router-link>|
      <router-link to="/create">Creat</router-link>|
      <router-link to="/join">joid</router-link>|
      <router-link to="/game">gabe</router-link>
    </div>
    <router-view/>
  </div>
</template>

<style lang="scss">
body {
  background: #f0edee;
}
// GLOBAL STYLES
@import url("https://fonts.googleapis.com/css?family=Limelight|Montserrat:400,400i,700");
*,
*::before,
*::after {
  font-family: "Limelight", cursive;
  box-sizing: border-box;
}
h1 {
  text-transform: uppercase;
}
select {
  text-align: center;
}
input {
  transition: .2s;
}
input:focus {
  outline: none;
  font-style: italic;
}
.button {
  width: 140px;
  height: 50px;
  font-size: 1rem;
  padding: 10px;
  margin: 20px 0;
  color: #2c666e;
  transition: 0.5s;
  position: relative;
  &:hover {
    color: #0a090c;
  }
  h3 {
    width: 100%;
    height: 125%;
    display: flex;
    justify-content: center;
    align-items: center;
    position: absolute;
    padding: 0;
    margin: 0;
    top: 0;
    left: 0;
    z-index: -1;
  }
  .button-border {
    position: absolute;
    top: 0;
    left: 0;
    .gold-layer > path {
      stroke: #2c666e !important;
      transition: 1s cubic-bezier(0.57, 0.21, 0.25, 1);
    }
    .green-layer > path {
      stroke: #2c666e !important;
      opacity: .5;
    }
    &:hover {
      .gold-layer > path {
        stroke-dasharray: 160;
        stroke: #E1AD21 !important;
        animation: border-stroke .7s cubic-bezier(0.41, 0.29, 0.58, 1);
        animation-delay: .05s;
      }
      .green-layer > path {
        opacity: .5;
      }
    }
  }
}
a {
  text-decoration: none;
}

#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
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

@keyframes border-stroke {
  from {
    stroke-dashoffset: 160
  }
  to {
    stroke-dashoffset: 0
  }
}


</style>
