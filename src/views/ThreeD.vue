<script setup>
// @ is an alias to /src
</script>

<template>
  <div class="three-d">
    <v-row justify="center" class="three-d-container" no-gutters>
      <v-col cols="8">
        <v-row no-gutters>
          <p class="title-text">3D</p>
        </v-row>
        <v-row no-gutters class="works-container">
          <v-col cols="4">
            <v-card class="card-1 cards-color"></v-card>
          </v-col>
          <v-col cols="8">
            <v-card class="card-2 cards-color"></v-card>
          </v-col>
          <v-col cols="8">
            <v-card class="card-3 cards-color"> </v-card>
          </v-col>
          <v-col cols="4">
            <v-card class="card-4 cards-color"> </v-card>
          </v-col>
          <v-col cols="4">
            <v-card class="card-1 cards-color"> </v-card>
          </v-col>
          <v-col cols="4">
            <v-card class="card-1 cards-color"> </v-card>
          </v-col>
          <v-col cols="4">
            <v-card class="card-1 cards-color"> </v-card>
          </v-col>
          <v-col cols="4">
            <v-card class="card-4 cards-color"> </v-card>
          </v-col>
          <v-col cols="8">
            <v-card class="card-3 cards-color"> </v-card>
          </v-col>
        </v-row>
      </v-col>
    </v-row>
  </div>
</template>

<style>
.three-d {
  background-color: #101010;
  width: 100%;
  height: 100%;
}
.three-d-container {
  padding-top: 5rem;
}
.title-text {
  font-family: Alata, sans-serif;
  font-size: 1.5rem;
  color: #c8c8c8;
  letter-spacing: 1rem;
  margin-left: 10rem;
  margin-bottom: 3rem;
}
.description-text {
  font-family: Alata, sans-serif;
  font-size: 1rem;
  color: #858585;
  letter-spacing: 0.1rem;
}
.description-container {
  padding-top: 2rem;
}
.card-1 {
  /* width: 19.3rem; */
  height: 27.7rem;
}
.card-2 {
  /* width: 40rem; */
  height: 27.7rem;
}
.card-3 {
  /* width: 40rem; */
  height: 19.3rem;
}
.card-4 {
  height: 19.3rem;
  /* width: 19.3rem; */
}
.cards-color {
  background-color: #313131;
  margin: 0.55rem;
  border-radius: 0;
}
</style>
