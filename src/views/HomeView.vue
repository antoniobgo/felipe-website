<script setup>
import router from "@/router";
import TestimonialCard from "@/components/TestimonialCard.vue";
</script>

<template>
  <div class="home">
    <div class="home-content-relative-position">
      <v-row no-gutters dense justify="center">
        <v-col cols="7">
          <v-row no-gutters dense justify="center">
            <v-card variant="outlined" class="video-container">
              <v-row justify="center" no-gutters dense>
                <v-btn
                  style="background-color: rgba(0, 0, 0, 0); z-index: 5"
                  variant="outlined"
                  flat
                  >motion designer, art director and 3d artist</v-btn
                >
              </v-row>
            </v-card>
          </v-row>
        </v-col>
      </v-row>
      <v-row no-gutters dense justify="center">
        <v-col cols="7">
          <v-row no-gutters dense justify="space-between">
            <v-col cols="5" class="pa-0">
              <v-card variant="outlined" class="other-videos-container">
              </v-card>
            </v-col>
            <v-col cols="5" class="pa-0">
              <v-card variant="outlined" class="other-videos-container">
              </v-card>
            </v-col>
          </v-row>
        </v-col>
      </v-row>
      <!-- <v-row no-gutters dense justify="center" class="latest-jobs-container">
        <p class="text-white size">LATEST JOBS</p>
      </v-row> -->
      <div>
        <v-row justify="center" align="center" class="intro-about-container">
          <v-col cols="6">
            <v-card variant="outlined" style="border-width: 0">
              <v-row no-gutters dense>
                <v-col cols="4">
                  <div class="ma-3 profile-pic-container">
                    <!-- <v-img
                      src="https://cdn.vuetifyjs.com/images/cards/foster.jpg"
                      cover
                    ></v-img>-->
                  </div>
                </v-col>
                <v-col cols="8" align-self="center">
                  <p class="ml-10 my-3 default-text">
                    Graduated Bachelor of Design in 2009
                  </p>
                  <p class="ml-10 my-3 default-text">
                    Motion designer since 2015
                  </p>
                  <p class="ml-10 my-3 default-text">
                    3d artist in his spare time since 2017
                  </p>
                  <v-btn
                    @click="router.push({ name: 'about' })"
                    flat
                    class="ml-10 font-menu about-button text-black"
                    color="#D2B100"
                    >ABOUT</v-btn
                  >
                </v-col>
              </v-row>
            </v-card>
          </v-col>
        </v-row>
        <div class="testimonials-container">
          <v-row justify="center">
            <p class="title-text title-margin">TESTIMONIALS</p>
          </v-row>
          <v-row justify="center" class="testimonials-card-container">
            <v-col cols="10">
              <v-row justify="center">
                <v-col cols="2">
                  <TestimonialCard></TestimonialCard>
                </v-col>
                <v-col cols="2">
                  <TestimonialCard></TestimonialCard>
                </v-col>
                <v-col cols="2">
                  <TestimonialCard></TestimonialCard>
                </v-col>
                <v-col cols="2">
                  <TestimonialCard></TestimonialCard>
                </v-col>
                <v-col cols="2">
                  <TestimonialCard></TestimonialCard>
                </v-col>
              </v-row>
            </v-col>
          </v-row>
        </div>
      </div>
    </div>
  </div>
</template>

<style>
.home {
  background: url("../assets/bg.png") no-repeat center;
  background-size: cover;
  width: 100%;
  height: 375vh;
}
.home-content-relative-position {
  position: relative;
  top: 95vh;
}
.video-container {
  width: 100%;
  height: 550px;
  border: solid 2px #474543;
  border-radius: 0px;
  z-index: 0;
}
.other-videos-container {
  max-width: 464x;
  height: 261px;
  border: solid 2px #474543;
  border-radius: 0px;
  margin-top: 15rem;
}
.latest-jobs-container {
  position: relative;
  top: 20vh;
}
.size {
  font-size: 2em;
  letter-spacing: 0.5em;
}
.title-margin {
  margin-top: 9rem;
}
.intro-about-container {
  margin-top: 20rem;
  height: 31.25rem;
  background-color: #151515;
}
.video-container-text-container {
  position: relative;
  bottom: 20px;
  z-index: 2;
  overflow: hidden;
}
.innertext {
  display: inline-block;
}
.profile-pic-container {
  width: 14.5rem;
  height: 19.25rem;
  background-color: #373737;
}
.testimonials-container {
  height: 31.25rem;
  background-color: #262626;
}
.testimonials-card-container {
  margin-top: 1rem;
}
.about-button {
  max-width: 6.25rem;
  max-height: 1.5rem;
  margin-top: 3rem;
}
</style>
