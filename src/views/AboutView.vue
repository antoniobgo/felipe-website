<script setup>
// @ is an alias to /src
</script>

<template>
  <div class="about">
    <v-row justify="center" class="about-container" no-gutters>
      <v-col cols="6">
        <v-row no-gutters>
          <p class="title-text">ABOUT</p>
        </v-row>
        <v-row no-gutters class="description-container">
          <p class="description-text">
            Designer graduated, motion designer senior and 3d student.
            Generalist, dedicated, responsive, experienced, loves to study and
            teamwork.responsive, experienced, loves to study and teamwork.
          </p>
        </v-row>
      </v-col>
    </v-row>
  </div>
</template>

<style>
.about {
  background-color: #101010;
  width: 100%;
  height: 100%;
}
.about-container {
  padding-top: 5rem;
}
.title-text {
  font-family: Alata, sans-serif;
  font-size: 1.5rem;
  color: #c8c8c8;
  letter-spacing: 1rem;
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
</style>
