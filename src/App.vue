<template>
  <div id="app">
    <div id="nav">
      <div class="wrapper-nav">
        <div class="title-logo">Portofolio</div>
        <ul>
          <li>
            <router-link to="/">Home</router-link>
          </li>
          <li>
            <router-link to="/about">About</router-link>
          </li>
          <li>
            <router-link to="/skills">Skills</router-link>
          </li>
        </ul>
      </div>
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
  position: absolute;
  width: 100%;
  height: 5rem;
  background: transparent;

  .wrapper-nav {
    display: flex;
    justify-content: space-between;
    align-items: center;
    max-width: 1376px;
    margin: 0 auto;
  }

  .title-logo {
    font-size: 1.5rem;
    padding-left: 1rem;
    color: #fbfafb;
  }

  a:hover {
    background-color: rgba(255, 255, 255, 0.2);
    border-radius: 0.1875rem;
    padding: 0.5rem 0.7rem;
  }

  a {
    text-transform: uppercase;
    padding: 0.5rem 0.7rem;
    font-size: 0.7142em;
    font-weight: bold;
    color: #fbfafb;

    &.router-link-exact-active {
      color: #e65858;
    }
  }

  ul {
    display: flex;
    justify-content: flex-end;
    margin: 0;
    padding: 1.5rem;

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
