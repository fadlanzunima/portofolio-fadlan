<template>
  <div class="about">
    <div class="content">
      <div class="container">
        <div class="card-container">
          <div class="row">
            <div class="about-me">
              <h1>About</h1>
              <p>
                Hello! I am Anthony Barnett. Web Developer, Graphic Designer and Photographer.
                Creative CV is a HTML resume template for professionals. Built with Bootstrap 4, Now UI Kit and FontAwesome, this modern and responsive design template is perfect to showcase your portfolio, skills and experience
              </p>
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
                  <tr>: Sicincin, 11 Maret 1996</tr>
                  <tr>: Tangerang</tr>
                  <tr>: (+62) 852 7809 1373</tr>
                  <tr>: fadlanzunima@gmail.com</tr>
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
export default {
  mounted: function() {
    this.showMenu = false;
  }
};
</script>

<style lang="scss" scoped>
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