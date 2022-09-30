<script setup>
import router from "@/router";
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
    <v-app-bar color="#181919" app flat height="62">
      <v-row class="pl-10" align="center" align-content="center">
        <v-btn class="mb-3">
          <div @click="onLogoClick" class="logo"></div>
        </v-btn>
        <p class="text-white app-bar-text">Felipe Miranda Gomes</p>
        <v-spacer />
        <v-spacer />
        <v-spacer />
        <v-spacer />
        <v-spacer />
        <v-btn @click="onMotionClick" class="mx-10 font-menu" color="#dbdbdb">
          Motion
        </v-btn>
        <v-btn @click="onThreeDClick" class="mx-10 font-menu" color="#dbdbdb">
          3D
        </v-btn>
        <v-btn @click="onAboutClick" class="mx-10 font-menu" color="#dbdbdb">
          About
        </v-btn>
        <v-btn @click="onContactClick" class="mx-10 font-menu" color="#dbdbdb">
          Contact
        </v-btn>
        <v-spacer />
      </v-row>
    </v-app-bar>
    <v-main>
      <router-view />
    </v-main>
    <v-footer app padless class="footer" absolute>
      <v-row no-gutters justify="center">
        <v-btn class="pa-0">
          <div class="linkedin"></div>
        </v-btn>
        <v-btn class="pa-0">
          <div class="ig"></div>
        </v-btn>
        <v-btn class="pa-0">
          <div class="vimeo"></div>
        </v-btn>
        <v-btn class="pa-0">
          <div class="youtube"></div>
        </v-btn>
        <v-btn class="pa-0">
          <div class="dot"></div>
        </v-btn>
        <v-divider color="#000000" class="my-5" />
        <v-row no-gutters justify="center">
          <p class="email-text">felipearaujodemirandagomes@gmail.com</p>
        </v-row>
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
.video-text {
  font-size: 1.875rem;
  line-height: 4.563rem;
  letter-spacing: 0.163rem;
}
.font-menu {
  color: #dbdbdb;
  font-size: 0.75rem;
  letter-spacing: 0.281rem;
  line-height: 1.035rem;
  font-weight: 400;
}
.second-title-text {
  font-size: 1.5rem;
  letter-spacing: 0.5rem;
  line-height: 2.063rem;
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
  color: #858585;
}
.default-text {
  font-size: 1rem;
  letter-spacing: 0.156rem;
  line-height: 2rem;
  color: #858585;
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
.logo {
  background: url("./assets/logo.svg") no-repeat center fixed;
  height: 3rem;
  width: 3rem;
}
.footer {
  height: 345px;
  background-color: #070707;
}
.linkedin {
  background: url("./assets/linkedin.png") no-repeat center fixed;
  height: 3rem;
  width: 4rem;
}
.youtube {
  background: url("./assets/youtube.png") no-repeat center fixed;
  height: 3rem;
  width: 4rem;
}
.vimeo {
  background: url("./assets/vimeo.png") no-repeat center fixed;
  height: 3rem;
  width: 4rem;
}
.dot {
  background: url("./assets/dot.png") no-repeat center fixed;
  height: 3rem;
  width: 4rem;
}
.ig {
  background: url("./assets/ig.png") no-repeat center fixed;
  height: 3rem;
  width: 4rem;
}
.email-text {
  font-size: 1rem;
  font-family: "Alata", sans-serif;
  letter-spacing: 0.2rem;
  color: #858585;
}
</style>
