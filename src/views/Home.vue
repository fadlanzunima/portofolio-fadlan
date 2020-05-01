<template>
  <div class="home">
    <div class="content">
      <div class="wrapper-content">
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
        <div class="wrapper-btn">
          <a class="btn-download" href="http://tiny.cc/fadlanCV" target="_blank">Download CV</a>
        </div>
        <div class="wrapper-social">
          <div
            class="btn-round"
            @click="goToSocialMedia('https://id.linkedin.com/in/fadlanzunima')"
          >
            <span class="tooltiptext">Follow me on LinkdIn</span>
            <i class="fab fa-linkedin"></i>
          </div>
          <div class="btn-round" @click="goToSocialMedia('https://www.facebook.com/fadlanzunima')">
            <span class="tooltiptext">Follow me on Facebook</span>
            <i class="fab fa-facebook"></i>
          </div>
          <div class="btn-round" @click="goToSocialMedia('https://twitter.com/alnzunima')">
            <span class="tooltiptext">Follow me on Twitter</span>
            <i class="fab fa-twitter"></i>
          </div>
          <div class="btn-round" @click="goToSocialMedia('https://www.instagram.com/fdlnzunima/')">
            <span class="tooltiptext">Follow me on Instagram</span>
            <i class="fab fa-instagram"></i>
          </div>
          <div class="btn-round" @click="goToSocialMedia('https://github.com/fadlanzunima/')">
            <span class="tooltiptext">Follow me on GitHub</span>
            <i class="fab fa-github"></i>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
// import HelloWorld from "@/components/HelloWorld.vue";

export default {
  data() {
    return {};
  },

  name: "Home",
  components: {
    // HelloWorld
  },

  methods: {
    goToSocialMedia(link) {
      window.location.href = link;
    },
    downloadCV() {}
  }
};
</script>

<style lang="scss" scoped>
.wrapper-content {
  position: relative;
  text-align: center;
  display: flex;
  flex-flow: column;
  justify-content: center;
  align-items: center;
  opacity: 1;
  animation: fade-in 1s linear;
}

@keyframes fade-in {
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}

.home::before {
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

.home {
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
    position: absolute;
    left: 50%;
    bottom: 25%;
    width: 100%;
    transform: translate(-50%, -25%);

    @media screen and (max-width: 1024px) {
      left: 50%;
      bottom: 20%;
      transform: translate(-50%, -20%);
    }
  }

  .img-user {
    width: auto;
    height: fit-content;

    img {
      border-radius: 50%;
      width: 9rem;
      height: 9rem;
      transition: all ease 1s;
      @media screen and (max-width: 320px) {
        width: 6rem;
        height: 6rem;
      }
    }

    img:hover {
      cursor: pointer;
      transform: scale(1.2);
      transition: all ease 1s;
    }
  }

  .txt-wrapper {
    text-align: center;

    h1 {
      font-size: 2.5em;
      padding-top: 1.3rem;
      margin-block-start: 0;
      margin-block-end: 0;

      @media screen and (max-width: 320px) {
        font-size: 1.5rem;
      }
    }

    h3 {
      letter-spacing: 1.5px;
      font-weight: 700;
      font-size: 1rem;
      padding-top: 0.5rem;
      text-transform: uppercase;
      margin-block-start: 0;
      margin-block-end: 0;
    }
  }

  .wrapper-btn {
    display: flex;
    margin-top: 1.5rem;
    justify-content: center;

    .btn-download {
      text-decoration: none;
      background-color: #378c3f;
      color: #fff;
      width: 10rem;
      height: 3rem;
      line-height: 3rem;
      border-width: 2px;
      font-weight: 400;
      font-size: 0.8571em;
      border-radius: 0.1875rem;
      cursor: pointer;
      transition: all ease 0.5s;

      &:hover {
        background-color: #40a249;
        transition: all ease 0.5s;
      }
    }
  }

  .wrapper-social {
    display: flex;
    flex-flow: row;
    position: absolute;
    bottom: -115px;

    @media screen and (max-width: 320px) {
      bottom: -80px;
    }

    .btn-round {
      cursor: pointer;
      display: flex;
      justify-content: center;
      align-items: center;
      width: 3.5rem;
      height: 3.5rem;
      border-radius: 50%;
      background-color: #888;
      margin: 0 1rem;

      @media screen and (max-width: 1024px) and (min-width: 330px) {
        width: 2.5rem;
        height: 2.5rem;
      }

      @media screen and (max-width: 320px) {
        width: 1.5rem;
        height: 1.5rem;
      }

      .svg-inline--fa {
        font-size: 2rem;
        @media screen and (max-width: 1024px) and (min-width: 330px) {
          font-size: 1rem;
        }

        @media screen and (max-width: 320px) {
          font-size: 0.8rem;
        }
      }

      &:hover {
        background-color: #979797;
        transform: scale(1.2);

        .tooltiptext {
          visibility: visible;
        }
      }

      .tooltiptext {
        visibility: hidden;
        width: 6rem;
        background-color: #888;
        color: #fff;
        font-size: 11px;
        text-align: center;
        border-radius: 6px;
        padding: 5px 0;

        /* Position the tooltip */
        position: absolute;
        z-index: 1;
        bottom: 115%;
        left: 50%;
        margin-left: -48px;
        @media screen and (max-width: 1024px) {
          width: 3rem;
          font-size: 7px;
          margin-left: -24px;
        }
      }

      .tooltiptext::after {
        content: "";
        position: absolute;
        top: 100%;
        left: 50%;
        margin-left: -5px;
        border-width: 5px;
        border-style: solid;
        border-color: #888 transparent transparent transparent;
      }
    }
  }
}
</style>
