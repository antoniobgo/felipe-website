<script setup>
import { ref } from "vue";
import router from "@/router";
import { useDisplay } from "vuetify";
import TestimonialCard from "@/components/TestimonialCard.vue";

const { mdAndUp } = useDisplay();
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
  <div class="home" :class="mdAndUp ? 'home-bg-desktop' : 'home-bg-mobile'">
    <div>
      <v-row no-gutters dense justify="center">
        <v-col
          cols="11"
          md="6"
          :class="mdAndUp ? 'reel-margin' : 'mobile-margin-1'"
        >
          <div
            class="video-container"
            :class="mdAndUp ? 'desktop-height' : 'reel-mobile-height'"
          >
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
        <v-col cols="11" md="6" :class="mdAndUp ? 'mt-15' : 'mobile-margin-2'">
          <v-card
            class="welcome-container"
            :class="
              mdAndUp
                ? 'welcome-container-desktop-height'
                : 'welcome-container-mobile-height'
            "
          >
            <v-row
              no-gutters
              dense
              justify="center"
              class="h-100"
              align="center"
            >
              <v-col cols="11" align-self="center">
                <div>
                  <p class="pb-3 text-center welcome-text">
                    WELCOME TO MY PORTFOLIO!
                  </p>
                  <p
                    class="text-center"
                    :class="mdAndUp ? 'welcome-text' : 'smaller-welcome-text'"
                  >
                    Here you will find my main works of motion design, art
                    direction and 3d artist.
                  </p>
                  <p
                    class="text-center"
                    :class="mdAndUp ? 'welcome-text' : 'smaller-welcome-text'"
                  >
                    And you can check my full profile on the about page.
                  </p>
                </div>
              </v-col>
            </v-row>
          </v-card>
        </v-col>
      </v-row>
      <v-row no-gutters dense justify="center">
        <v-col cols="11" md="3">
          <div :class="mdAndUp ? 'mr-3' : ''">
            <v-hover v-slot="{ isHovering, props }">
              <v-card
                @click="router.push({ name: 'motion' })"
                :height="mdAndUp ? '670px' : '150px'"
                class="video-container"
                :class="
                  isHovering
                    ? mdAndUp
                      ? 'motion-video-container-onhover mt-15'
                      : 'motion-video-container-onhover-mobile mobile-margin-2'
                    : mdAndUp
                    ? 'motion-video-container mt-15'
                    : 'motion-video-container-mobile mobile-margin-2'
                "
                v-bind="props"
              >
                <v-row class="h-100" no-gutters dense justify="center">
                  <v-col cols="12" align-self="end">
                    <p class="video-text text-center text-yellow">MOTION</p>
                  </v-col>
                  <v-col cols="12" align-self="end">
                    <div v-show="isHovering" class="onhover-area">
                      <v-row no-gutters dense justify="center">
                        <v-col cols="10">
                          <p class="text-center small-card-font mt-3">
                            Softwares: After Effects, Premier, Ilustrator and
                            photoshop
                          </p>
                        </v-col>
                      </v-row>
                    </div>
                  </v-col>
                </v-row>
              </v-card>
            </v-hover>
          </div>
        </v-col>
        <v-col cols="11" md="3">
          <div :class="mdAndUp ? 'ml-3' : ''">
            <v-hover v-slot="{ isHovering, props }">
              <v-card
                @click="router.push({ name: 'three-d' })"
                :height="mdAndUp ? '670px' : '150px'"
                class="video-container"
                :class="
                  isHovering
                    ? mdAndUp
                      ? 'threed-video-container-onhover mt-15'
                      : 'threed-video-container-onhover-mobile mobile-margin-2'
                    : mdAndUp
                    ? 'threed-video-container mt-15'
                    : 'threed-video-container-mobile mobile-margin-2'
                "
                v-bind="props"
              >
                <v-row class="h-100" no-gutters dense justify="center">
                  <v-col cols="12" align-self="end">
                    <p class="video-text text-center text-yellow">3D</p>
                  </v-col>
                  <v-col cols="12" align-self="end">
                    <div v-show="isHovering" class="onhover-area">
                      <v-row no-gutters dense justify="center">
                        <v-col cols="10">
                          <p class="text-center small-card-font mt-3">
                            Softwares: Blender and Unreal, Photoshop and After
                            Efects for post.
                          </p>
                        </v-col>
                      </v-row>
                    </div>
                  </v-col>
                </v-row>
              </v-card>
            </v-hover>
          </div>
        </v-col>
      </v-row>
      <div style="background: black">
        <div
          :class="
            mdAndUp
              ? 'intro-about-container-desktop'
              : 'intro-about-container-mobile mobile-margin-3'
          "
        >
          <v-row no-gutters class="h-100" justify="center">
            <v-col cols="8" md="3">
              <div class="profile-pic-container"></div>
            </v-col>
            <v-col cols="4" md="4" align-self="center">
              <div :class="mdAndUp ? '' : 'experience-container-position'">
                <p
                  :class="
                    mdAndUp
                      ? 'ml-10 mb-10 second-title-text'
                      : 'smaller-second-title-text'
                  "
                >
                  EXPERIENCE
                </p>
                <p
                  :class="
                    mdAndUp
                      ? 'ml-10 experience-default-text'
                      : 'experience-smaller-default-text mobile-margin-2'
                  "
                >
                  Visual Designer since 2006
                </p>
                <p
                  :class="
                    mdAndUp
                      ? 'ml-10 experience-default-text'
                      : 'experience-smaller-default-text'
                  "
                >
                  Motion designer since 2015
                </p>
                <p
                  :class="
                    mdAndUp
                      ? 'ml-10 experience-default-text'
                      : 'experience-smaller-default-text'
                  "
                >
                  3d artist in his spare time since 2017
                </p>
                <p
                  :class="
                    mdAndUp
                      ? 'ml-10 experience-default-text'
                      : 'experience-smaller-default-text'
                  "
                >
                  UX designer since 2021
                </p>
                <v-btn
                  @click="router.push({ name: 'about' })"
                  flat
                  class="text-black rounded-0"
                  :class="
                    mdAndUp
                      ? 'about-button ml-10 mt-10'
                      : 'mobile-about-button mobile-margin-2'
                  "
                  color="#D2B100"
                  >ABOUT</v-btn
                >
              </div>
            </v-col>
          </v-row>
        </div>
        <div
          class="testimonials-container"
          :class="
            mdAndUp
              ? 'testimonials-desktop-height'
              : 'testimonials-mobile-height'
          "
        >
          <v-row no-gutters justify="center">
            <p
              :class="
                mdAndUp
                  ? 'second-title-text testimonial-margin-desktop'
                  : 'testimonial-title-mobile mobile-margin-4'
              "
            >
              TESTIMONIALS
            </p>
          </v-row>
          <v-row
            no-gutters
            justify="center"
            class="testimonials-card-container"
          >
            <v-col cols="11" md="3">
              <TestimonialCard
                :testimonialContent="testimonialsContent[0]"
              ></TestimonialCard>
            </v-col>
            <v-col v-if="!mdAndUp" class="horizontal-line-divider" cols="3">
            </v-col>
            <v-col
              cols="11"
              md="3"
              :class="mdAndUp ? 'testimonial-border' : ''"
            >
              <TestimonialCard
                :testimonialContent="testimonialsContent[1]"
              ></TestimonialCard>
            </v-col>
            <v-col v-if="!mdAndUp" class="horizontal-line-divider" cols="3">
            </v-col>
            <v-col cols="11" md="3">
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
  width: 100%;
  height: 100%;
}
.home-bg-mobile {
  background: url("../assets/bg_mobile.png") center;
  background-size: cover;
}
.home-bg-desktop {
  background: url("../assets/bg.png") no-repeat;
}

.desktop-height {
  height: 550px;
}
.mobile-height {
  height: 176px;
}
.reel-mobile-height {
  height: 230px;
}
.video-internal-container {
  width: 100%;
  height: 100%;
  background-clip: content-box;
}
.videoreel-row {
  width: 95%;
  height: 95%;
}
.welcome-container {
  border: solid 2px #191919;
  border-radius: 0px;
  z-index: 0;
  background: radial-gradient(50% 50% at 50% 50%, #15150e 0%, #0b0a03 100%);
  padding: 6px;
  background-clip: content-box;
}
.welcome-container-mobile-height {
  height: 150px;
}
.welcome-container-desktop-height {
  height: 200px;
}
.video-container {
  border-radius: 0px;
  padding: 6px;
  border: solid 2px #191919;
  background-clip: content-box;
}
.threed-video-container {
  background-image: linear-gradient(rgba(0, 0, 0, 0.5), rgba(0, 0, 0, 0.5)),
    url("../assets/threed_bg.png");
}
.threed-video-container-onhover {
  background-image: linear-gradient(rgba(0, 0, 0, 0), rgba(0, 0, 0, 0)),
    url("../assets/threed_bg.png");
}
.threed-video-container-mobile {
  background-image: linear-gradient(rgba(0, 0, 0, 0.5), rgba(0, 0, 0, 0.5)),
    url("../assets/threed_bg_mobile.png");
}
.threed-video-container-onhover-mobile {
  background-image: linear-gradient(rgba(0, 0, 0, 0), rgba(0, 0, 0, 0)),
    url("../assets/threed_bg_mobile.png");
}

.motion-video-container {
  background-image: linear-gradient(rgba(0, 0, 0, 0.9), rgba(0, 0, 0, 0.5)),
    url("../assets/motion_bg.png");
}
.motion-video-container-onhover {
  background-image: linear-gradient(rgba(0, 0, 0, 0), rgba(0, 0, 0, 0)),
    url("../assets/motion_bg.png");
}
.motion-video-container-mobile {
  background-image: linear-gradient(rgba(0, 0, 0, 0.9), rgba(0, 0, 0, 0.5)),
    url("../assets/motion_bg_mobile.png");
}
.motion-video-container-onhover-mobile {
  background-image: linear-gradient(rgba(0, 0, 0, 0), rgba(0, 0, 0, 0)),
    url("../assets/motion_bg_mobile.png");
}
.latest-jobs-container {
  position: relative;
  top: 20vh;
}
.reel-margin {
  margin-top: 5rem;
}
.intro-about-container-desktop {
  margin-top: 10rem;
  background: url("../assets/experience_bg.png") center;
  background-size: auto;
  height: 460px;
}
.intro-about-container-mobile {
  background: black;
  height: 230px;
}
.profile-pic-container {
  width: 100%;
  height: 100%;
  background: url("../assets/experience_profile.png") center;
  background-size: cover;
}
.experience-container-position {
  position: relative;
  right: 40px;
}
.onhover-area {
  height: 108px;
  background-color: rgba(210, 177, 0, 0.66);
}
.testimonials-container {
  background-color: #121212;
}
.testimonials-mobile-height {
  height: 680px;
}
.testimonials-desktop-height {
  height: 470px;
}
.testimonials-card-container {
  margin-top: 1rem;
}
.testimonial-margin-desktop {
  margin-top: 7rem;
  margin-bottom: 2.5rem;
}
.about-button {
  width: 100px;
  max-height: 25px;
  font-size: 0.75rem;
  line-height: 1rem;
  letter-spacing: 0.28rem;
}
.about-button:hover {
  cursor: pointer;
  width: 120px;
  font-weight: 500;
  height: 30px;
  font-size: 1rem;
  line-height: 1.1rem;
}
.mobile-about-button {
  width: 70px;
  max-height: 17px;
  font-size: 0.5rem;
  line-height: 0.7rem;
  letter-spacing: 0.18rem;
}
.horizontal-line-divider {
  width: 100%;
  border-top: solid 1px #747474;
}
.vertical-line-divider {
  height: 100%;
  width: 0%;
  border-right: solid 1px #747474;
}

.testimonial-border {
  border-left: solid 1px #747474;
  border-right: solid 1px #747474;
}
.testimonial-mobile-border {
  border-top: solid 1px #747474;
  border-bottom: solid 1px #747474;
}
</style>
