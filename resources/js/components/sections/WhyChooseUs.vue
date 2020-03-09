<template>
  <b-container class="why-choose-us">
    <b-row>
      <b-col>
        <h3 class="text-primary">
          Why Choose Us
        </h3>
        <h1>The Right Choice for Quality Home Improvement for More Than 35 Years</h1>

        <p>
          If you're in the market for a Dayton, Northern Cincinnati, OH, roofer, our experienced team is ready to
          help. At D & G Roofing & Restoration, we understand that a roof is more than simply another part of your
          property. It also protects your loved ones and the valuable belongings that make your house a home. We have
          helped many people throughout Dayton and Northern Cincinnati, OH, address their roofing needs with
          efficiency and ease. We're ready to use our extensive experience to help you do the same. Regardless, of the
          nature of the project, our crew will begin as soon as possible, and we’ll complete the job in a timely
          manner. Your satisfaction is one of our highest priorities.
        </p>
        <b-container fluid>
          <b-row>
            <b-col md="4">
              <a href="http://www.homeadvisor.com/c.Gutters.Dayton.OH.-12038.html#spid=39451675"
                 style="display: block; margin: 0 auto;"
              >
                <b-img alt="Elite Customer Service - D&G Roofing and Restoration, LLC"
                       src="http://www.homeadvisor.com/images/sp-badges/elite-solid-border.png?sp=39451675&key=251b6e36da24ee0f78ca80ad6e3acf64"
                />
              </a>
            </b-col>
            <b-col md="4">
              <b-img alt="Shingle Master - D&G Roofing and Restoration, LLC"
                     src="dist/img/shingle-master.png"
              />
            </b-col>
            <b-col md="4">
              <b-img alt="BBB - D&G Roofing and Restoration, LLC"
                     src="dist/img/bbb.png"
              />
            </b-col>
          </b-row>
        </b-container>
      </b-col>
      <b-col>
        <b-img class="gerri" src="dist/img/gerri-transparent-bg.png" alt="Gerri Transparent Image" fluid-grow />
      </b-col>
    </b-row>
  </b-container>
</template>

<style lang="scss" scoped>
  .why-choose-us {
    position: relative;
    margin-bottom: 50px;

    .gerri {
      position: absolute;
      bottom: -57px;
      left: 25%;
      z-index: -1;
    }

    &:before {
      content: url('/dist/img/figure/clip9.png');
      position: absolute;
      right: -100px;
      top: 15%;
      transform: translateY(-50%);
      line-height: 0;
      z-index: -1;
    }

    &:after {
      content: url('/dist/img/figure/clip4.png');
      position: absolute;
      bottom: -50px;
      left: -250px;
      line-height: 0;
    }
  }
</style>

<script>
export default {}
</script>
