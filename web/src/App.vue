<template>
  <div id="app">
    <div id="nav">
      <h2>Mijn Reis</h2>
    </div>
    <router-view/>
  </div>
</template>

<style lang="scss">
html, body {
  padding: none;
  margin: none;
}

#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin: 0;
}

#nav {
  background-color: #ffc917;
  padding: 10px;
  display: flex;
  justify-content: space-between;
  text-align: center;
  align-items: center;

  a, h2 {
    color: #003082;
    text-decoration: none;
    font-weight: bold;
    font-size: 18px;
    font-family: segoe ui;
  }

}
</style>
