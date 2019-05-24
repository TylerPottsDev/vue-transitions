<template>
  <div id="app">
    <div id="nav">
      <router-link to="/">Home</router-link> |
      <router-link to="/about">About</router-link>
    </div>
    <transition name="view">
      <router-view />
    </transition>
  </div>
</template>

<style>
body {
  margin: 0;
  padding: 0;
  background: #F3F3F3;
}
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  padding: 15px;
}
#nav {
  padding: 30px;
}

#nav a {
  color: #2c3e50;
  font-size: 20px;
  text-decoration: none;
}

#nav a.router-link-exact-active {
  color: #ffce00;
}

.page {
  display: block;
  margin: 0 auto;
  width: 100%;
  max-width: 768px;
  padding: 15px;
  box-sizing: border-box;
}

.view-enter-active, .view-leave-active {
  transition: opacity 0.5s ease-in-out, transform 0.5s ease;
}

.view-enter-active {
  transition-delay: 0.5s;
}

.view-enter {
  opacity: 0;
  transform: translateY(-100px);
}
.view-enter-to {
  opacity: 1;
  transform: translateY(0px);
}
.view-leave {
  opacity: 1;
  transform: translateY(0px);
}

.view-leave-to {
  opacity: 0;
  transform: translateY(100px);
}
</style>
