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

      <div class="wrapper-mobile">
        <div class="wrapper-nav">
          <div class="title-logo">Portofolio</div>
          <div class="logo-bars">
            <i class="fas fa-bars"></i>
          </div>
        </div>
        <div id="myLinks">
          <a href="#news">News</a>
          <a href="#contact">Contact</a>
          <a href="#about">About</a>
        </div>
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

  @media screen and (max-width: 1024px) {
    width: 22.5rem;
    height: 40rem;
    overflow: hidden;
  }
}

#nav {
  position: absolute;
  width: 100%;
  height: 5rem;
  background: transparent;

  //MOBILE NAV
  .wrapper-mobile {
    display: none;

    @media screen and (max-width: 1024px) {
      display: block;
      width: 30rem;
    }

    .wrapper-mobile a {
      color: white;
      padding: 14px 16px;
      text-decoration: none;
      font-size: 17px;
      display: block;
    }

    .wrapper-nav {
      @media screen and (max-width: 1024px) {
        display: flex;
        flex-flow: row;
        justify-content: space-between;
        padding-top: 10px;
        margin: 0px 5px;
      }
    }

    .logo-bars {
      display: flex;
      justify-content: center;
      align-items: center;
      background: #fff;
      width: 2rem;
      height: 2rem;
      border-radius: 5px;

      .svg-inline--fa {
        color: black;
        font-size: 1rem;
      }
    }
  }
  //MOBILE NAV

  .wrapper-nav {
    display: flex;
    justify-content: space-between;
    align-items: center;
    max-width: 1376px;
    margin: 0 auto;

    @media screen and (max-width: 1024px) {
      display: none;
    }
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
