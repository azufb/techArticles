<template>
  <div id="nav">
    <div class="navBar">
      <h1>Let's Try Sass!</h1>
      <div class="naviMenu">
        <router-link to="/">Home</router-link> |
        <router-link to="/about">About</router-link>
      </div>
    </div>
    <router-view />
  </div>
</template>

<style>
body {
  margin: 0;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

.navBar {
  padding: 15px 30px;
  background-color: #2c3e50;
  display: flex;
  align-items: center;
  position: relative;
}

.naviMenu {
  position: absolute;
  right: 30px;
}

h1 {
  color: #fff;
}

#nav a {
  font-weight: bold;
  color: #fff;
}

#nav a.router-link-exact-active {
  color: #42b983;
}
</style>
