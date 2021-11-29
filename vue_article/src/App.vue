<template>
  <div id="nav">
    <div class="navBar">
      <h1 class="title">Try Sass</h1>
      <div class="naviMenu">
        <router-link to="/">Home</router-link> |
        <router-link to="/about">About</router-link>
      </div>
    </div>
    <router-view />
  </div>
</template>

<style lang="scss">
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
  background-color: #4b7eb1;
  display: flex;
  align-items: center;
  position: relative;
  height: 10vh;
}

.title {
  color: #fff;
}

.naviMenu {
  position: absolute;
  right: 30px;
}

#nav {
  height: 100vh;
}

#nav a {
  font-weight: bold;
  color: #fff;
}

#nav a.router-link-exact-active {
  color: #2c3e50;
}
</style>
