<template>
  <div class="home">
    <div class="bg-content">
      <div class="img-user">
        <img
          src="https://media-exp1.licdn.com/dms/image/C5103AQG7PA4Sq3hnVA/profile-displayphoto-shrink_200_200/0?e=1593648000&v=beta&t=QrvXyqp1Hx-Aqz6u0Lf6OJFlNG2FRjpSVDly2euD5wA"
          alt="img"
        />
      </div>
      <div class="txt-wrapper">
        <h1>Fadlan Zunima</h1>
        <h3>Frontend Developer</h3>
      </div>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
// import HelloWorld from "@/components/HelloWorld.vue";

export default {
  name: "Home",
  components: {
    // HelloWorld
  }
};
</script>

<style lang="scss" scoped>
.home {
  display: flex;
  justify-content: center;
  align-items: center;
  min-height: 49vw;
  color: #2b2734;

  .bg-content {
    display: flex;
    justify-content: center;
    align-items: center;
    background: #ffff;
  }

  .img-user {
    width: 13rem;
    height: fit-content;
    border-radius: 50%;
    img {
      border-radius: 50%;
    }
  }

  .txt-wrapper {
    text-align: left;
  }
}
</style>
