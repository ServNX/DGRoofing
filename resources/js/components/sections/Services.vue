<template>
  <b-container class="services bg-dark" fluid>
    <b-container class="services-content">
      <b-row class="d-flex justify-content-center">
        <h3 class="text-primary">
          What We Do
        </h3>
      </b-row>
      <b-row class="d-flex justify-content-center">
        <h1 class="text-light">
          Services We Provide
        </h1>
      </b-row>
      <b-row class="mt-5">
        <b-col lg="4">
          <div class="service-card">
            <b-img src="dist/img/service-roof-repair.jpg" fluid alt="Responsive image" />
            <div class="card-overlay text-center text-light">
              <h1>
                Roof Repair
              </h1>
              <p>
                A nice little description here!
              </p>
            </div>
          </div>
        </b-col>
        <b-col lg="4">

        </b-col>
        <b-col lg="4">

        </b-col>
        <b-col lg="4">

        </b-col>
        <b-col lg="4">

        </b-col>
        <b-col lg="4">

        </b-col>
      </b-row>
    </b-container>

  </b-container>
</template>

<style lang="scss" scoped>
  @import "../../../sass/variables";

  .services {
    margin: 0;
    padding: 100px 0 50px;

    .services-content {
      .service-card {
        width: 370px;
        height: 285px;
        overflow: hidden;
        border-radius: 4px;
        margin-bottom: 30px;

        img {
          transition: 1s;
        }

        &:hover {
          img {
            transform: scale(1.2);
          }

          .card-overlay {
            transform: translateY(-50px);
          }
        }

        .card-overlay {
          padding: 10px;
          background-color: rgba($red, 0.7);
          position: relative;
          top: -60px;
          transition: 0.5s;
        }
      }
    }
  }
</style>

<script>
export default {
  components: {}
}
</script>
