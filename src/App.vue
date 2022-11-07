<script setup>
import router from "@/router";
import { useDisplay } from "vuetify";

const { mdAndUp } = useDisplay();
const onAboutClick = function () {
  router.push({ name: "about" });
};
const onThreeDClick = function () {
  router.push({ name: "three-d" });
};
const onMotionClick = function () {
  router.push({ name: "motion" });
};
const onContactClick = function () {
  router.push({ name: "contact" });
};
const onLogoClick = function () {
  router.push({ name: "home" });
};
</script>
<template>
  <v-app class="font">
    <v-app-bar color="#181919" app flat height="64">
      <div
        class="d-flex w-100"
        :class="mdAndUp ? 'justify-space-between' : 'justify-space-between'"
      >
        <div class="d-flex align-center" :class="mdAndUp ? 'ml-15' : 'ml-5'">
          <div @click="onLogoClick" class="logo"></div>
          <p v-if="mdAndUp" class="pl-4 text-white app-bar-text">
            Felipe Miranda Gomes
          </p>
        </div>
        <div
          class="d-flex align-center"
          :class="mdAndUp ? 'mr-10 justify-space-around' : 'mr-5 ml-2'"
        >
          <v-btn
            @click="onMotionClick"
            :class="mdAndUp ? 'mx-10 font-menu' : 'smaller-font-menu'"
            color="#dbdbdb"
            :size="mdAndUp ? '' : 'small'"
          >
            Motion
          </v-btn>
          <v-btn
            @click="onThreeDClick"
            :class="mdAndUp ? 'mx-10 font-menu' : 'smaller-font-menu'"
            color="#dbdbdb"
            :size="mdAndUp ? '' : 'x-small'"
          >
            3D
          </v-btn>
          <v-btn
            @click="onAboutClick"
            :class="mdAndUp ? 'mx-10 font-menu' : 'smaller-font-menu'"
            color="#dbdbdb"
            :size="mdAndUp ? '' : 'small'"
          >
            About
          </v-btn>
          <v-btn
            @click="onContactClick"
            :class="mdAndUp ? 'mx-10 font-menu' : 'smaller-font-menu'"
            color="#dbdbdb"
            :size="mdAndUp ? '' : 'small'"
          >
            Contact
          </v-btn>
        </div>
      </div>
    </v-app-bar>
    <v-main>
      <router-view />
    </v-main>
    <v-footer app :class="mdAndUp ? 'footer' : 'mobile-footer'" absolute>
      <v-row dense no-gutters justify="center">
        <v-col align="start" cols="12" md="7">
          <v-row dense no-gutters justify="center" class="pb-5">
            <form action="https://www.linkedin.com/in/felipe-miranda-gomes/">
              <button class="footer-button linkedin" type="submit" />
            </form>
            <form action="https://www.instagram.com/_felipemirandagomes/">
              <button class="footer-button ig" type="submit" />
            </form>
            <form action="https://vimeo.com/felipegomesmotiondesign">
              <button class="footer-button vimeo" type="submit" />
            </form>
            <form
              action="https://www.youtube.com/channel/UC4fvA-TpNIE3GUwiPWUvbnQ"
            >
              <button class="footer-button youtube" type="submit" />
            </form>
            <form action="https://www.flickr.com/photos/felipemirando/">
              <button class="footer-button dot" type="submit" />
            </form>
          </v-row>
        </v-col>
        <v-col cols="11">
          <p class="email-text text-center my-4">
            felipearaujodemirandagomes@gmail.com
          </p>
        </v-col>
        <v-col cols="11">
          <v-row justify="center" no-gutters dense>
            <div class="mb-4 footer-line"></div>
          </v-row>
        </v-col>
        <v-col cols="11">
          <p class="email-text text-center">web development by Antonio Gomes</p>
        </v-col>
      </v-row>
    </v-footer>
  </v-app>
</template>

<style>
.font {
  font-family: "Alata", sans-serif;
}
.welcome-text {
  font-size: 0.875rem;
  font-weight: 400;
  line-height: 1.44rem;
  letter-spacing: 0.13rem;
  color: #cdcdcd;
}
.testimonial-title-mobile {
  font-size: 0.875rem;
  letter-spacing: 0.5rem;
  line-height: 1.2rem;
  color: #c8c8c8;
}
.smaller-welcome-text {
  font-size: 0.625rem;
  line-height: 1.03rem;
  letter-spacing: 0.09rem;
  color: #cdcdcd;
}
.video-text {
  font-size: 1.875rem;
  line-height: 2rem;
  letter-spacing: 0.163rem;
}
.font-menu {
  color: #dbdbdb;
  font-size: 0.75rem;
  letter-spacing: 0.281rem;
  line-height: 1.035rem;
  font-weight: 400;
}
.smaller-font-menu {
  color: #dbdbdb;
  font-size: 0.5rem;
  letter-spacing: 0.281rem;
  line-height: 0.68rem;
  font-weight: 400;
}
.small-card-font {
  font-size: 1.125rem;
  line-height: 1.875rem;
  letter-spacing: 0.113rem;
}
.second-title-text {
  font-size: 1.5rem;
  letter-spacing: 0.5rem;
  line-height: 2.063rem;
  color: #c8c8c8;
}
.smaller-second-title-text {
  font-size: 0.875rem;
  letter-spacing: 0.271rem;
  line-height: 1.2rem;
  color: #c8c8c8;
}
.font-title {
  font-weight: 400;
  font-size: 1.5rem;
  line-height: 2.07rem;
  letter-spacing: 0.75rem;
  color: #c8c8c8;
}
.citation-text {
  font-size: 0.75rem;
  font-weight: 400;
  font-style: italic;
  line-height: 1.625rem;
  letter-spacing: 0.125rem;
  color: #c8c8c8;
}
.smaller-citation-text {
  font-size: 0.7rem;
  font-style: italic;
  line-height: 1.125rem;
  letter-spacing: 0.125rem;
  color: #c8c8c8;
}
.smaller-testimonial-text {
  font-size: 0.68rem;
  line-height: 1.03rem;
  letter-spacing: 0.125rem;
  color: #c8c8c8;
}
.testimonial-text {
  font-size: 0.75rem;
  font-weight: 400;
  line-height: 1.625rem;
  letter-spacing: 0.125rem;
  color: #c8c8c8;
}
.default-text {
  font-size: 1rem;
  letter-spacing: 0.156rem;
  line-height: 2rem;
  color: #858585;
}
.smaller-default-text {
  font-size: 0.6rem;
  line-height: 1.125rem;
  color: #858585;
}
.experience-default-text {
  font-size: 1rem;
  letter-spacing: 0.156rem;
  line-height: 2rem;
  color: #c8c8c8;
}
.experience-smaller-default-text {
  font-size: 0.6rem;
  line-height: 1.125rem;
  color: #c8c8c8;
}
.app-bar-text {
  font-family: Bakbak One, sans-serif;
  font-weight: 500;
  letter-spacing: 0.0892857143em;
  text-indent: 0.0892857143em;
  text-transform: uppercase;
  line-height: normal;
  font-weight: 500;
}
.mobile-margin-1 {
  margin-top: 30px;
}
.mobile-margin-2 {
  margin-top: 15px;
}
.mobile-margin-3 {
  margin-top: 40px;
}
.mobile-margin-4 {
  margin-top: 60px;
}
.logo {
  background: url("./assets/logo.svg") no-repeat center fixed;
  height: 62px;
  width: 35px;
}
.logo:hover {
  cursor: pointer;
}
.footer {
  height: 345px;
  background-color: #070707;
}
.mobile-footer {
  height: 230px;
  background-color: #070707;
}
.linkedin {
  background: url("./assets/linkedin.png") no-repeat center fixed;
}
.youtube {
  background: url("./assets/youtube.png") no-repeat center fixed;
}
.vimeo {
  background: url("./assets/vimeo.png") no-repeat center fixed;
}
.footer-button {
  height: 40px;
  width: 60px;
  margin: 0 4px 0 4px;
}
.footer-button:hover {
  cursor: pointer;
}
.dot {
  background: url("./assets/dot.png") center;
}
.ig {
  background: url("./assets/ig.png") no-repeat center fixed;
}
.email-text {
  font-size: 0.75rem;
  letter-spacing: 0.09rem;
  color: #858585;
}
.footer-line {
  height: 1px;
  width: 50px;
  border-top: 1px solid #858585;
}
</style>
