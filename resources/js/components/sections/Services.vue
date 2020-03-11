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
          Our Services
        </h1>
      </b-row>
      <b-row class="mt-5">
        <b-col v-for="service in services" :key="service.title" lg="4">
          <div class="service-card">
            <b-img :src="service.img" fluid-grow :alt="service.title" />
            <div class="card-overlay text-center text-light">
              <h1>
                {{ service.title }}
              </h1>
              <p>
                {{ service.desc }}
              </p>
            </div>
          </div>
        </b-col>
      </b-row>
    </b-container>
  </b-container>
</template>

<style lang="scss" scoped>
  @import "../../../sass/variables";

  .services {
    position: relative;
    padding: 50px;
    margin: 0;
    z-index: 1;

    @media only screen and (min-width: $sm) {
      padding: 100px 50px;
    }

    @media only screen and (min-width: $xl) {
      &:before {
        content: url('/dist/img/figure/clip8.png');
        position: absolute;
        right: 0;
        bottom: 0;
        line-height: 0;
        filter: grayscale(1);
        z-index: -1;
      }

      &:after {
        content: url('/dist/img/figure/clip7.png');
        position: absolute;
        left: 0;
        top: 50%;
        transform: translateY(-50%);
        line-height: 0;
        filter: grayscale(1);
        z-index: -1;
      }
    }

    .services-content {

      .service-card {
        height: 225px;
        overflow: hidden;
        border-radius: 4px;
        margin-bottom: 30px;

        @media only screen and (min-width: $xl) {
          height: 285px;
        }

        img {
          transition: 1s;
          filter: grayscale(0.7);
        }

        &:hover {
          img {
            transform: scale(1.2);
            filter: none;
          }

          .card-overlay {
            transform: translateY(-50px);
          }
        }

        .card-overlay {
          height: 130px;
          padding: 10px;
          background-color: rgba($red, 0.7);
          position: relative;
          transition: 0.5s;

          @media only screen and (min-width: $sm) {
            top: -230px;
          }

          @media only screen and (min-width: $md) {
            top: -370px;
          }

          @media only screen and (min-width: $lg) {
            top: -60px;
          }

          @media only screen and (min-width: $xl) {
            top: -50px
          }
        }
      }
    }
  }
</style>

<script>
export default {
  data: () => ({
    services: [
      {
        img: 'dist/img/service-roofing.jpg',
        title: 'Roofing',
        desc: 'A nice little description goes here.'
      },
      {
        img: 'dist/img/service-siding.jpg',
        title: 'Siding',
        desc: 'A nice little description goes here.'
      },
      {
        img: 'dist/img/service-windows.jpg',
        title: 'Windows',
        desc: 'A nice little description goes here.'
      },
      {
        img: 'dist/img/service-gutters.jpg',
        title: 'Gutters',
        desc: 'A nice little description goes here.'
      },
      {
        img: 'dist/img/service-roofing.jpg',
        title: 'Doors',
        desc: 'A nice little description goes here.'
      },
      {
        img: 'dist/img/service-roofing.jpg',
        title: 'Commercial',
        desc: 'A nice little description goes here.'
      }
    ]
  })
}
</script>
