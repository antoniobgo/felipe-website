<script setup>
import { ref } from "vue";
// import router from "@/router";
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
          <v-card class="welcome-container">
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
          <v-card class="motion-video-container mr-3">
            <v-row class="h-100" no-gutters dense justify="center">
              <v-col align-self="center">
                <p class="video-text text-center text-yellow">MOTION</p>
              </v-col>
            </v-row>
          </v-card>
        </v-col>
        <v-col cols="3">
          <v-card class="threed-video-container ml-3">
            <v-row class="h-100" no-gutters dense justify="center">
              <v-col align-self="center">
                <p class="video-text text-center text-yellow">3D</p>
              </v-col>
            </v-row>
          </v-card>
        </v-col>
      </v-row>
      <div>
        <div style="height: 470px" class="intro-about-container">
          <v-row class="h-100" justify="center">
            <v-col cols="3">
              <div class="profile-pic-container"></div>
            </v-col>
            <v-col cols="4" align-self="center">
              <p class="ml-10 mb-10 second-title-text">EXPERIENCE</p>
              <p class="ml-10 default-text">Visual Designer since 2006</p>
              <p class="ml-10 default-text">Motion designer since 2015</p>
              <p class="ml-10 default-text">
                3d artist in his spare time since 2017
              </p>
              <p class="ml-10 default-text">UX designer since 2021</p>
              <v-btn
                @click="router.push({ name: 'about' })"
                flat
                class="ml-10 font-menu about-button text-black"
                color="#D2B100"
                >ABOUT</v-btn
              >
            </v-col>
          </v-row>
        </div>
        <div class="testimonials-container">
          <v-row justify="center">
            <p class="second-title-text testimonial-margin">TESTIMONIALS</p>
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
  height: 100%;
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
  padding: 8px;
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
  padding: 8px;
  background-clip: content-box;
}
.threed-video-container {
  background: url("../assets/threed_bg.png");
  height: 670px;
  border: solid 2px #474543;
  border-radius: 0px;
  margin-top: 10px;
  background-clip: content-box;
  padding: 8px;
  filter: brightness(50%);
}
.motion-video-container {
  background: url("../assets/motion_bg.png");
  height: 670px;
  border: solid 2px #474543;
  border-radius: 0px;
  margin-top: 10px;
  background-clip: content-box;
  padding: 8px;
  filter: brightness(50%);
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
  background: url("../assets/experience_bg.png");
}
.profile-pic-container {
  width: 100%;
  height: 100%;
  background: url("../assets/experience_profile.png");
  background-size: cover;
}
.testimonials-container {
  height: 470px;
  background-color: #121212;
}
.testimonials-card-container {
  margin-top: 1rem;
}
.testimonial-margin {
  margin-top: 7rem;
}
.about-button {
  max-width: 6.25rem;
  max-height: 1.5rem;
  margin-top: 3rem;
}
</style>
