<template>
  <div class="about">
    <div class="bg-content"></div>
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
</template>


<style lang="scss" scoped>
.about {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
  color: #fff;

  .container {
    max-width: 1024px;
  }

  .card-container {
    border: 0;
    border-radius: 0.1875rem;
    display: inline-block;
    position: relative;
    overflow: hidden;
    width: 100%;
    word-wrap: break-word;
    background-color: rgba(255, 255, 255, 0.7);
    background-clip: border-box;

    .row {
      display: flex;
      flex-flow: row;
      padding: 10px;
      width: fit-content;
      height: 25rem;
      color: #2c2c2c;

      h1 {
        font-weight: 700;
        color: black;
        font-size: 2rem;
      }

      p {
        font-size: 1.1rem;
        line-height: 40px;
      }

      .about-me {
        width: 50%;
        padding: 10px;
        text-align: left;
      }

      .basic-info {
        width: 50%;
        text-align: left;
        padding: 10px;

        table {
          line-height: 2;
        }

        td:nth-child(1) {
          font-weight: 600;
          text-transform: uppercase;
        }

        td:nth-child(2) {
          padding-left: 2rem;
        }

        tr {
          font-size: 1.1rem;
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