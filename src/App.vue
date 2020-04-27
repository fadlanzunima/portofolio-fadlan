<template>
  <div id="app">
    <div id="nav">
      <ul>
        <li>
          <router-link to="/">Home</router-link>
        </li>
        <li>
          <router-link to="/about">About</router-link>
        </li>
      </ul>
    </div>
    <router-view />
  </div>
</template>

<style lang="scss">
#app {
  padding: 0;
  margin: 0;
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #fbfafb;
}

#nav {
  width: 100%;
  height: 6rem;
  background: #b0acbe;

  a {
    font-weight: bold;
    color: #fbfafb;

    &.router-link-exact-active {
      color: #486789;
    }
  }

  ul {
    display: flex;
    justify-content: flex-end;
    margin: 0;
    padding: 2rem;

    li {
      margin-left: 30px;
      list-style: none;
      font-size: 1.5rem;

      a {
        text-decoration: none;
      }
    }
  }
}
</style>
