<script setup>
import { ref } from "vue";
import router from "@/router";
import TestimonialCard from "@/components/TestimonialCard.vue";

const testimonialsContent = ref([
  {
    name: "Rocha",
    jobTitle: "Mormaii Motorsports",
    content:
      "“Um mix de criatividade e sinceridade, adoramos trabalhar com Felipe.”",
  },
  {
    name: "Braz",
    jobTitle: "Motion Head agência 300",
    content:
      "“Muito assertivo nas entregas, boa leitura de briefing, trabalha bem em equipe.”",
  },
  {
    name: "Luiz",
    jobTitle: "Video editor and vfx job partner",
    content:
      "“Grande diretor de arte, motion designer, parceiro para os bons e maus momentos.”",
  },
]);
</script>

<template>
  <div class="home">
    <div>
      <v-row no-gutters dense justify="center">
        <v-col cols="6" class="title-margin">
          <div class="video-container">
            <div class="video-internal-container">
              <iframe
                src="https://www.youtube.com/embed/50ELR5bF5QY"
                frameborder="0"
                style="height: 100%; width: 100%"
                allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture"
                allowfullscreen
              ></iframe>
            </div>
          </div>
        </v-col>
      </v-row>
      <v-row no-gutters dense justify="center">
        <v-col cols="6" class="mt-15">
          <v-card variant="outlined" class="welcome-container">
            <v-row
              no-gutters
              dense
              justify="center"
              class="h-100"
              align="center"
            >
              <v-col cols="10" align-self="center">
                <p class="text-center welcome-text">WELCOME TO MY PORTFOLIO!</p>
                <p class="text-center welcome-text">
                  Here you will find my main works of motion design, art
                  direction and 3d artist.
                </p>
                <p class="text-center welcome-text">
                  And you can check my full profile on the about page.
                </p>
              </v-col>
            </v-row>
          </v-card>
        </v-col>
      </v-row>
      <v-row no-gutters dense justify="center">
        <v-col cols="3">
          <v-card variant="outlined" class="other-videos-container mr-3">
          </v-card>
        </v-col>
        <v-col cols="3">
          <v-card variant="outlined" class="other-videos-container ml-3">
          </v-card>
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
            <v-col cols="2">
              <TestimonialCard
                :testimonialContent="testimonialsContent[0]"
              ></TestimonialCard>
            </v-col>
            <v-col cols="2">
              <div
                style="
                  border-left: solid 1px #747474;
                  border-right: solid 1px #747474;
                "
              >
                <TestimonialCard
                  :testimonialContent="testimonialsContent[1]"
                ></TestimonialCard>
              </div>
            </v-col>
            <v-col cols="2">
              <TestimonialCard
                :testimonialContent="testimonialsContent[2]"
              ></TestimonialCard>
            </v-col>
          </v-row>
        </div>
      </div>
    </div>
  </div>
</template>

<style>
.home {
  background: url("../assets/bg.png") center;
  background-size: cover !important;
  width: 100%;
  padding-top: 62px;
  /* height: 100%; */
}
.video-container {
  position: relative;
  height: 550px;
  border: solid 2px #474543;
  border-radius: 0px;
}
.video-internal-container {
  width: 100%;
  height: 100%;
  background-clip: content-box; /* support: IE9+ */
  /* background-color: #ccc; */
  padding: 10px 10px 10px 10px !important;
}
.videoreel-row {
  width: 95%;
  height: 95%;
}
.welcome-container {
  height: 150px;
  border: solid 2px #474543;
  border-radius: 0px;
  z-index: 0;
  background: radial-gradient(50% 50% at 50% 50%, #15150e 0%, #0b0a03 100%);
  padding: 10px;
  background-clip: content-box;
}
.other-videos-container {
  height: 670px;
  border: solid 2px #474543;
  border-radius: 0px;
  margin-top: 10px;
}
.latest-jobs-container {
  position: relative;
  top: 20vh;
}
.title-margin {
  margin-top: 5rem;
}
.intro-about-container {
  margin-top: 10rem;
  height: 470px;
  background-color: #151515;
}
.profile-pic-container {
  width: 14.5rem;
  height: 19.25rem;
  background-color: #373737;
}
.testimonials-container {
  height: 470px;
  background-color: #121212;
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
