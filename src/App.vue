<template>
  <div id="app">
    <b-navbar type="dark" variant="dark">
      <b-navbar-brand href="./Home">
        <img
          src="https://i.pinimg.com/originals/bd/41/0c/bd410c791d8598fc0b92afe5f9d96d03.png"
          class="d-inline-block align-top"
          alt="Amiya"
          height="75"
        />
        Amiya-Shop
      </b-navbar-brand>
    </b-navbar>
    <router-view />
  </div>
</template>
<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
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
