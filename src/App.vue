<script setup>
import router from "@/router";
const onAboutClick = function () {
  router.push({ name: "about" });
};
const onThreeDClick = function () {
  router.push({ name: "three-d" });
};
</script>
<template>
  <v-app>
    <v-app-bar color="#181919" app flat>
      <v-row class="pl-10" align="center">
        <div class="logo"></div>
        <p class="text-white app-bar-text">Felipe Miranda Gomes</p>
        <v-spacer></v-spacer>
        <v-btn class="mx-10 text-white"> Motion </v-btn>
        <v-btn @click="onThreeDClick" class="mx-10 text-white"> 3D </v-btn>
        <v-btn @click="onAboutClick" class="mx-10 text-white"> About </v-btn>
        <v-btn class="mx-10 text-white"> Contact </v-btn>
      </v-row>
    </v-app-bar>
    <v-main>
      <router-view />
    </v-main>
    <v-footer app padless class="footer" absolute>
      <v-row no-gutters justify="center">
        <v-btn variant="outlined" class="mx-10 text-white"> ue </v-btn>
        <v-btn class="mx-10 text-white"> 3D </v-btn>
        <v-btn class="mx-10 text-white"> About </v-btn>
        <v-btn class="mx-10 text-white"> Contact </v-btn>
        <v-divider color="#858585" class="my-10" />
        <v-col cols="12">
          <v-row no-gutters justify="center">
            <p class="email-text">felipearaujodemirandagomes@gmail.com</p>
          </v-row>
        </v-col>
      </v-row>
    </v-footer>
  </v-app>
</template>

<style>
.app-bar-text {
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
  height: 15rem;
  background-color: #070707;
}
.email-text {
  font-size: 1rem;
  font-family: "Alata", sans-serif;
  letter-spacing: 0.2rem;
  color: #858585;
}
</style>
