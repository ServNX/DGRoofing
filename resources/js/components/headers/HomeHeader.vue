<template>
  <b-container class="home-header" fluid>
    <b-container class="header-content">
      <b-row>
        <b-col xl="6">
          <h1 class="d-sm-none text-light">
            D & G Roofing
          </h1>

          <h1 class="d-none d-sm-block text-light">
            Roofing Experts
          </h1>

          <p class="d-none d-sm-block">
            When you're in the market for a Dayton, OH, roofing company, our knowledgeable crew is here to provide you
            with high caliber work. At D & G Roofing & Restoration, we're prepared to act as your first and final
            resource when it comes to all your roofing needs. When you're ready to take the next step, we're excited for
            the opportunity to help you benefit from our thorough attention to detail.
          </p>
        </b-col>
        <b-col class="d-none d-xl-block" xl="6">
          <b-container class="header-form bg-light">
            <div class="item-heading text-center">
              <h3 class="item-title">
                Request An Inspection
              </h3>
            </div>
            <b-form>
              <b-form-group label="Email address:"
                            label-for="input-1"
                            description="We'll never share your email with anyone else."
              >
                <b-form-input id="input-1" type="email" required placeholder="Enter email" />
              </b-form-group>

              <b-form-group label="Your Name:" label-for="input-2">
                <b-form-input id="input-2" required placeholder="Enter name" />
              </b-form-group>

              <b-form-group label="Your Phone:" label-for="input-3">
                <b-form-input id="input-3" required placeholder="Enter phone" />
              </b-form-group>

              <b-form-group label="How did you hear about us:" label-for="input-4">
                <b-form-select id="input-4" v-model="source" :options="sources" required />
              </b-form-group>

              <b-button type="submit" variant="primary">
                Submit
              </b-button>
              <b-button type="reset" variant="light">
                Reset
              </b-button>
            </b-form>
          </b-container>
        </b-col>
      </b-row>
    </b-container>
  </b-container>
</template>

<style lang="scss" scoped>
  @import "../../../sass/variables";

  .home-header {
    height: 90px;
    background-image: linear-gradient(to right, rgba(0, 0, 0, 0.6), rgba(0, 0, 0, 0.2)), url('/dist/img/home-main.jpg');

    @media only screen and (min-width: $sm) {
      height: 400px;
    }

    @media only screen and (min-width: $lg) {
      height: 600px;
    }

    .header-content {
      z-index: 1;
      position: relative;
      top: 8%;
      color: $white;
      font-weight: 700;
      line-height: 30px;

      @media only screen and (min-width: $md) {
        top: 15%;
      }

      @media only screen and (min-width: $lg) {
        top: 25%;
      }

      h1 {
        font-size: 30px;
        background-color: rgba(238, 27, 37, 0.6);
        display: inline-block;
        padding: 20px 25px;
        clip-path: polygon(8% 0, 100% 0%, 92% 100%, 0% 100%);

        @media only screen and (min-width: $sm) {
          font-size: 60px;
          padding: 20px 40px;
        }

        @media only screen and (min-width: $md) {
          padding: 20px 55px;
        }

        @media only screen and (min-width: $lg) {
          padding: 20px 75px;
        }

        @media only screen and (min-width: $xl) {
          padding: 20px 45px;
        }
      }

      h2 {
        font-size: 40px;
      }

      p {
        font-size: 18px;
        font-weight: 100;
        margin-bottom: 20px;
        background-color: rgba(45, 45, 45, 0.8);
        padding: 10px;
      }

      .header-form {
        width: 390px;
        color: $dark;
        padding: 25px;
        transform: translateY(-20%);
        border-radius: 4px;
        line-height: normal;
        margin-right: 0;
      }
    }
  }
</style>

<script>
export default {
  components: {},
  data: () => ({
    source: null,
    sources: [{ text: 'Select One', value: null }, 'Google', 'Friend', 'Yard Sign', 'Paper', 'Mailer', 'Other']
  })
}
</script>
