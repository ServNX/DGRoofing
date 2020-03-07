<template>
  <b-container class="home-header" fluid>
    <b-img class="header-img" src="dist/img/home-main.jpg" alt="Home Main Header Image" fluid-grow />
    <b-container class="header-img-overlay" fluid />

    <b-container class="header-content">
      <b-row>
        <b-col>
          <h1 class="text-light">
            Expert
          </h1>
          <h2>Roofing Contractor</h2>
          <p>
            When you're in the market for a Dayton, OH, roofing company, our knowledgeable crew is here to provide you
            with high caliber work. At D & G Roofing & Restoration, we're prepared to act as your first and final
            resource when it comes to all your roofing needs. When you're ready to take the next step, we're excited for
            the opportunity to help you benefit from our thorough attention to detail.
          </p>
        </b-col>
        <b-col>
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
    padding: 0;
    margin-bottom: 100px;
    height: 600px;
    position: relative;

    .header-img {
      transform: scale(1);
      height: 100%;
    }

    .header-img-overlay {
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background-image: linear-gradient(to right, rgba(0, 0, 0, 0.6), rgba(0, 0, 0, 0.2));
    }

    .header-content {
      z-index: 100;
      position: absolute;
      top: 25%;
      right: calc((100% - 1170px) / 2);
      color: $white;
      font-weight: 700;
      line-height: 30px;

      h1 {
        font-size: 60px;
      }

      h2 {
        font-size: 40px;
      }

      p {
        font-size: 18px;
        font-weight: 100;
        margin-bottom: 20px;
      }

      .header-form {
        width: 390px;
        color: $dark;
        padding: 25px;
        transform: translateY(-20%);
        border-radius: 4px;
        line-height: normal;
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
