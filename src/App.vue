<template>
  <div id="app">
    <div class="flex-box">
      <div class="flex-box-header">后台管理</div>
      <div class="flex-box-body">
        <div class="flex-box-body left">
          <div class="ui inverted vertical pointing0 menu">
            <router-link class="item" to="/">Home</router-link>
            <router-link class="item" to="/project">Project</router-link>
            <router-link class="item" to="/about">About</router-link>
          </div>
        </div>
        <div class="flex-box-body right">
          <div id="main">
            <router-view/>
          </div>
        </div>
      </div>
      <div class="flex-box-footer"></div>
    </div>
  </div>
</template>

<style lang="scss">
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
</style>
 