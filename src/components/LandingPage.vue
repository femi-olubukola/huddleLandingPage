<template>
  <div class="page">
    <div>
      <div class="tw-hidden lg:tw-block">
        <v-img :src="backgroundImage" style="height: 100vh">
          <div class="logo tw-pl-16 tw-mt-14">
            <img :src="huddleLogo" alt=""/>
          </div>

          <div class="tw-flex">
            <div class="illustrationLogo tw-pl-16 tw-mt-24">
              <img class="illustrationImg" :src="illustration"/>
            </div>

            <div class="tw-mt-36 tw-pl-36">
              <div class="headingText">Build The Community <br/> Your Fans Will Love</div>
              <div class="miniText tw-mt-5"> Huddle reimagines the way we build communities. You have <br/>
                a voice, but so does your audience. Create connections with <br/>
                your users as you engage in genuine discussion.</div>

              <div class="tw-mt-5">
                <v-btn style="border-radius: 30px ; background-color: #E882E8 ; color: white; width: 200px; height: 60px; font-size: large" class="text-capitalize">Register</v-btn>
              </div>
            </div>

          </div>

          <div class="tw-justify-end tw-items-end tw-flex tw-mr-24 tw-mt-28">

            <v-hover
                v-slot="{ hover }"
                open-delay="200"
            >
            <v-btn :color="hover ? '' : '#674BAF'"
                   :class="{ 'on-hover': hover }" icon outlined class="white--text tw-mr-5 tw-w-12">
              <v-icon>mdi-facebook</v-icon>
            </v-btn>

            </v-hover>

            <v-btn icon outlined class="white--text tw-mr-5">
              <v-icon>mdi-twitter</v-icon>
            </v-btn>
            <v-btn icon outlined class="white--text">
              <v-icon>mdi-instagram</v-icon>
            </v-btn>

          </div>


        </v-img>
      </div>


<!--      <div-->
<!--          :style="{-->
<!--        'background-image': `url(${require(image)})`,-->
<!--        width: '100px',-->
<!--        height: '100px',-->
<!--        position: 'relative'-->
<!--      }"-->
<!--      ></div>-->

      <div class="md:tw-hidden">
        <img :src="mobileBackgroundImage"/>
      </div>
    </div>
  </div>
</template>

<script>
  export default {
    name: 'LandingPage',

    data () {
      return {
        image: "@/assets/bg-desktop.svg",
        backgroundImage: require(`/src/assets/bg-desktop.svg`),
        mobileBackgroundImage: require(`/src/assets/bg-mobile.svg`),
        huddleLogo: require(`/src/assets/logo.svg`),
        illustration: require(`/src/assets/illustration-mockups.svg`),
      }
  }


  }
</script>

<style scoped>

.page {
  background-color: #674BAF;
  background-image: url("/src/assets/bg-desktop.svg");
  background-size: cover;
  height: 100vh;
  /*position: relative;*/
  background-repeat: no-repeat;
  background-position:center;
}

/*.illuImg {*/
/*  width: 830px;*/
/*  height: 500px;*/
/*}*/

.button {
  color: #E882E8;
}

.headingText {
  font-family: "Poppins", sans-serif;
  font-weight: 600;
  font-size: 50px;
  /*line-height: 140%;*/
  font-style: normal;
  /*display: flex;*/
  /*align-items: */
  color: white;
}

.miniText {
  font-family: "Open Sans", sans-serif;
  font-weight: 400;
  font-size: 22px;
  font-style: normal;
  color: white;
}
.v-btn .on-hover {
  color: red !important;
}
</style>
