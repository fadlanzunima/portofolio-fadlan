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
          <li>
            <router-link to="/projects">Projects</router-link>
          </li>
        </ul>
      </div>

      <div class="topnav">
        <a href="#home" class="active">Portofolio</a>
        <div id="myLinks" ref="dropdown" @click="onLeave()">
          <router-link to="/">Home</router-link>
          <router-link to="/about">About</router-link>
          <router-link to="/skills">Skills</router-link>
          <router-link to="/projects">Projects</router-link>
        </div>
        <a href="javascript:void(0)" class="icon" @mouseover="onOver">
          <i class="fa fa-bars"></i>
        </a>
      </div>
    </div>
    <router-view />
  </div>
</template>

<script>
export default {
  data: function() {
    return {
      showMenu: false
    };
  },
  methods: {
    onOver() {
      this.$refs.dropdown.style.display = "block";
    },
    onLeave() {
      this.$refs.dropdown.style.display = "none";
    }
  }
};
</script>

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

  //MOBILE NAV
  .topnav {
    display: none;
    @media screen and(max-width: 1024px) {
      display: block;
      overflow: hidden;
      background-color: #333;
      position: relative;
    }
  }

  #myLinks {
    display: none;
  }

  .topnav a {
    color: white;
    padding: 14px 16px;
    text-decoration: none;
    font-size: 17px;
    display: block;
  }

  .topnav a.icon {
    background: black;
    display: block;
    position: absolute;
    right: 0;
    top: 0;
  }

  .topnav a:hover {
    background-color: #ddd;
    color: black;
    padding: 14px;
  }

  .active {
    background-color: #4caf50;
    color: white;
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
