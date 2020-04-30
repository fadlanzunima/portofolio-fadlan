<template>
  <div class="skills">
    <div class="content">
      <div class="container">
        <div class="card">
          <div class="title-content">Familiar With</div>
          <div class="row">
            <div class="wrapper">
              <div class="wrapper-bar">
                <div class="wrapper-title">
                  <div class="title">HTML</div>
                  <div class="title">90%</div>
                </div>
                <div class="meter">
                  <span style="width: 90%"></span>
                </div>
              </div>
              <div class="wrapper-bar">
                <div class="wrapper-title">
                  <div class="title">CSS</div>
                  <div class="title">90%</div>
                </div>
                <div class="meter">
                  <span style="width: 90%"></span>
                </div>
              </div>
              <div class="wrapper-bar">
                <div class="wrapper-title">
                  <div class="title">JQUERY</div>
                  <div class="title">90%</div>
                </div>
                <div class="meter">
                  <span style="width: 90%"></span>
                </div>
              </div>
              <div class="wrapper-bar">
                <div class="wrapper-title">
                  <div class="title">vuejs</div>
                  <div class="title">80%</div>
                </div>
                <div class="meter">
                  <span style="width: 80%"></span>
                </div>
              </div>
            </div>
            <div class="wrapper">
              <div class="wrapper-bar">
                <div class="wrapper-title">
                  <div class="title">Scss</div>
                  <div class="title">85%</div>
                </div>
                <div class="meter">
                  <span style="width: 85%"></span>
                </div>
              </div>
              <div class="wrapper-bar">
                <div class="wrapper-title">
                  <div class="title">JSON</div>
                  <div class="title">70%</div>
                </div>
                <div class="meter">
                  <span style="width: 70%"></span>
                </div>
              </div>
              <div class="wrapper-bar">
                <div class="wrapper-title">
                  <div class="title">axios</div>
                  <div class="title">80%</div>
                </div>
                <div class="meter">
                  <span style="width: 80%"></span>
                </div>
              </div>
              <div class="wrapper-bar">
                <div class="wrapper-title">
                  <div class="title">ANGULAR</div>
                  <div class="title">60%</div>
                </div>
                <div class="meter">
                  <span style="width: 60%"></span>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import $ from "jquery";

export default {
  mounted() {
    this.progressBar();
  },

  methods: {
    progressBar() {
      $(".meter > span").each(function() {
        $(this)
          .data("origWidth", $(this).width())
          .width(0)
          .animate(
            {
              width: $(this).data("origWidth") // or + "%" if fluid
            },
            1200
          );
      });
    }
  }
};
</script>

<style lang="scss" scoped>
.skills::before {
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

.skills {
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

    @media screen and (max-width: 1024px) {
      padding-top: 0rem;
    }

    .container {
      width: 1024px;

      @media screen and (max-width: 1024px) {
        width: 330px;
      }

      .card {
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
          height: 130vmin;
          overflow: scroll;
        }

        .title-content {
          padding: 10px;
          color: black;
          font-weight: 600;
        }

        .row {
          display: flex;
          flex-flow: row;
          padding: 15px;
          width: auto;
          height: 25rem;
          color: #2c2c2c;

          @media screen and (max-width: 1024px) {
            flex-flow: column;
            align-items: center;
            width: 100%;
            height: 100%;
            padding: unset;
          }
          .wrapper {
            width: 100%;
            padding-right: 1rem;

            @media screen and (max-width: 1024px) {
              padding: 1rem;
              margin-bottom: -35px;
              width: 90%;
              height: 100%;
            }
            .wrapper-bar {
              text-align: left;
              margin-top: 10px;
              margin-bottom: 3rem;

              .wrapper-title {
                display: flex;
                justify-content: space-between;
              }

              @media screen and (max-width: 1024px) {
                margin-bottom: 1.5rem;
              }

              .title {
                padding-bottom: 10px;
                color: black;
                font-weight: 600;
                font-size: 0.8571em;
                text-transform: uppercase;
              }

              .meter > span:after,
              .animate > span > span {
                animation: move 2s linear infinite;
              }

              @keyframes move {
                0% {
                  background-position: 0 0;
                }
                100% {
                  background-position: 50px 50px;
                }
              }

              .meter {
                height: 15px; /* Can be anything */
                position: relative;
                -moz-border-radius: 25px;
                -webkit-border-radius: 25px;
                border-radius: 25px;
                padding-bottom: 10px;
              }

              .meter > span {
                display: block;
                height: 100%;
                border-top-right-radius: 8px;
                border-bottom-right-radius: 8px;
                border-top-left-radius: 20px;
                border-bottom-left-radius: 20px;
                background-color: rgb(43, 194, 83);
                background-image: linear-gradient(
                  center bottom,
                  rgb(43, 194, 83) 37%,
                  rgb(84, 240, 84) 69%
                );
                box-shadow: inset 0 2px 9px rgba(255, 255, 255, 0.3),
                  inset 0 -2px 6px rgba(0, 0, 0, 0.4);
                position: relative;
                overflow: hidden;
              }

              .meter > span:after {
                content: "";
                position: absolute;
                top: 0;
                left: 0;
                bottom: 0;
                right: 0;
                background-image: linear-gradient(
                  -45deg,
                  rgba(255, 255, 255, 0.2) 25%,
                  transparent 25%,
                  transparent 50%,
                  rgba(255, 255, 255, 0.2) 50%,
                  rgba(255, 255, 255, 0.2) 75%,
                  transparent 75%,
                  transparent
                );
                z-index: 1;
                background-size: 50px 50px;
                animation: move 2s linear infinite;
                border-top-right-radius: 8px;
                border-bottom-right-radius: 8px;
                border-top-left-radius: 20px;
                border-bottom-left-radius: 20px;
                overflow: hidden;
              }
            }
          }
        }
      }
    }
  }
}
</style>