<template>
  <div id="app">
    <div id="nav">

    </div>
    <router-view/>
  </div>
</template>

<script>
  export default {
    name: 'App',
    created () {
      setTimeout(() => {
        window.L2Dwidget.init({
          pluginRootPath: 'static/live2dw/',
          pluginJsPath: 'lib/',
          pluginModelPath: 'live2d-widget-model-hijiki/assets/',
          tagMode: false,
          debug: false,
          model: { jsonPath: '/static/live2dw/live2d-widget-model-hijiki/assets/hijiki.model.json' },
          display: { position: 'right', width: 150, height: 350 },
          mobile: { show: true },
          log: false
        })
      }, 1000)
    }
  }
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  width: 100%;
  height: 0;
  cursor: url("./assets/mouse.png"),auto;
}
*{
  margin: 0;
  padding: 0;
}
#nav {
  padding: 30px;
}

#nav a {
  font-weight: bold;
  color: #2c3e50;
}

#nav a.router-link-exact-active {
  color: #42b983;
}

</style>
