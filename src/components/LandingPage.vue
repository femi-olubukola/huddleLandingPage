<template>
  <div class="page">
    <div>
      <div class="tw-hidden lg:tw-block">
        <v-img :src="backgroundImage" style="height: 100vh">
          <div class="logo tw-pl-16 tw-mt-14">
            <img :src="huddleLogo"/>
          </div>

          <div class="tw-flex">
            <div class="illustrationLogo tw-pl-16 tw-mt-24">
              <img class="illustrationImg" :src="illustration"/>
            </div>

            <div class="tw-mt-40 tw-pl-40">
              <div class="headingText">Build The Community <br/> Your Fans Will Love</div>
              <div class="miniText"> Huddle reimagines the way we build communities. You have <br/>
                a voice, but so does your audience. Create connections with <br/>
                your users as you engage in genuine discussion.</div>

              <div>
                <v-btn style="border-radius: 12px ; background-color: #E882E8 ; color: white">Register</v-btn>
              </div>
            </div>

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
  font-family: Poppins;
  font-weight: 600;
  font-size: 50px;
  /*line-height: 140%;*/
  font-style: normal;
  /*display: flex;*/
  /*align-items: */
  color: white;
}

.miniText {
  font-family: Open-Sans;
  font-weight: 400;
  font-size: 22px;
  font-style: normal;
  color: white;
}
</style>
