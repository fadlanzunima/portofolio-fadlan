<template>
  <div class="about">
    <div class="content">
      <div class="container">
        <div class="loading" v-if="isLoading">
          <div class="fancy-spinner">
            <div class="ring"></div>
            <div class="ring"></div>
            <div class="dot"></div>
          </div>
        </div>
        <div class="card-container" v-if="!isLoading">
          <div class="row" v-for="(about, index) in arrayAbout" :key="index">
            <div class="about-me">
              <h1>About</h1>
              <p>{{about.about_desc}}</p>
            </div>
            <div class="basic-info">
              <h1>Basic Information</h1>
              <table>
                <td>
                  <tr>Place, Date of Birth</tr>
                  <tr>Address</tr>
                  <tr>Phone</tr>
                  <tr>Email</tr>
                </td>
                <td>
                  <tr>: {{about.about_date_of_birth}}</tr>
                  <tr>: {{about.about_adress}}</tr>
                  <tr>: {{about.about_phone}}</tr>
                  <tr>
                    :
                    <a v-bind:href="'mailto:' + about.about_adress">{{about.about_email}}</a>
                  </tr>
                </td>
              </table>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>


<script>
import axios from "axios";
export default {
  data() {
    return {
      isLoading: false,
      arrayAbout: []
    };
  },

  mounted: function() {
    this.fetchAbout();
  },
  methods: {
    fetchAbout() {
      this.isLoading = true;
      axios
        .get(
          "http://www.mocky.io/v2/5eaa733a2d00006b0026862d?mocky-delay=1000ms"
        )
        .then(response => {
          this.arrayAbout = response.data.result;
          this.isLoading = false;
        });
    }
  }
};
</script>

<style lang="scss" scoped>
//LOADING
$charade: #282a37;
$bluebell: #979fd0;

.loading {
  background: transparent;
}

.fancy-spinner {
  display: flex;
  justify-content: center;
  align-items: center;
  width: 5rem;
  height: 5rem;

  div {
    position: absolute;
    width: 4rem;
    height: 4rem;
    border-radius: 50%;

    &.ring {
      border-width: 0.5rem;
      border-style: solid;
      border-color: transparent;
      animation: 2s fancy infinite alternate;

      &:nth-child(1) {
        border-left-color: $bluebell;
        border-right-color: $bluebell;
      }
      &:nth-child(2) {
        border-top-color: $bluebell;
        border-bottom-color: $bluebell;
        animation-delay: 1s;
      }
    }

    &.dot {
      width: 1rem;
      height: 1rem;
      background: $bluebell;
    }
  }
}

@keyframes fancy {
  to {
    transform: rotate(360deg) scale(0.5);
  }
}
//LOADING

.about::before {
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

.about {
  position: absolute;
  display: block;
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
    padding-top: 1rem;
  }

  .container {
    max-width: 1024px;

    @media screen and (max-width: 1024px) {
      max-width: 330px;
    }
  }

  @keyframes fade-in {
    from {
      background-color: rgba(255, 255, 255, 0);
    }
    to {
      background-color: rgba(255, 255, 255, 0.7);
    }
  }

  .card-container {
    border: 0;
    border-radius: 0.1875rem;
    display: inline-block;
    position: relative;
    overflow: hidden;
    width: 100%;
    word-wrap: break-word;
    background-clip: border-box;
    background-color: rgba(255, 255, 255, 0.7);
    animation: fade-in 1s linear;

    @media screen and (max-width: 1024px) {
      border: unset;
      border-radius: unset;
      display: block;
      background-clip: unset;
    }

    .row {
      display: flex;
      flex-flow: row;
      padding: 10px;
      width: fit-content;
      height: 25rem;
      color: #2c2c2c;

      @media screen and (max-width: 1024px) {
        flex-flow: column;
        align-items: center;
        width: 100%;
        height: 100%;
        padding: unset;
      }

      h1 {
        font-weight: 700;
        color: black;
        font-size: 2rem;
        margin-block-end: 0;
        margin-block-start: 0;
      }

      p {
        font-size: 1.1rem;
        line-height: 40px;

        @media screen and (max-width: 1024px) {
          font-size: 0.8rem;
          margin-block-end: 0;
          margin-block-start: 0;
        }
      }

      .about-me {
        width: 50%;
        padding: 10px;
        text-align: left;

        @media screen and (max-width: 1024px) {
          width: 90%;
          height: 100%;
        }
      }

      .basic-info {
        width: 50%;
        text-align: left;
        padding: 10px;

        @media screen and (max-width: 1024px) {
          width: 90%;
          height: 100%;
        }

        table {
          line-height: 2;
        }

        td:nth-child(1) {
          font-weight: 600;
          text-transform: uppercase;
        }

        td:nth-child(2) {
          padding-left: 2rem;

          @media screen and (max-width: 1024px) {
            padding-left: 0.5rem;
          }
        }

        tr {
          font-size: 1.1rem;
          @media screen and (max-width: 1024px) {
            font-size: 0.7rem;
          }

          a {
            text-decoration: none;
            color: inherit;
          }
        }
      }
    }
  }
}

.bg-content::before {
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

.bg-content {
  display: flex;
  justify-content: center;
  align-items: center;
  background: url(https://images.pexels.com/photos/814499/pexels-photo-814499.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=750&w=1260);
  position: absolute;
  background-size: cover;
  background-position: center center;
  width: 100%;
  height: 100%;
  z-index: -1;
}
</style>