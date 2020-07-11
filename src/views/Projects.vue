<template>
  <div class="projects">
    <div class="content"></div>
  </div>
</template>

<style lang="scss" scoped>
.projects::before {
  position: absolute;
  background-color: rgba(0, 0, 0, 0.4);
  z-index: 0;
  width: 100%;
  height: 100%;
  display: block;
  left: 0;
  top: 0;
  content: "";
}

.projects {
  position: absolute;
  display: block;
  color: #fff;
  background: url(https://images.pexels.com/photos/814499/pexels-photo-814499.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=750&w=1260);
  background-size: cover;
  background-position: center center;
  width: 100%;
  height: 100%;
  z-index: -1;

  .content {
    height: 100%;
    display: flex;
    justify-content: center;
    align-items: center;
  }
}
</style>