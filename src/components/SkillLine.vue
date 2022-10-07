<script setup>
import { ref, defineProps } from "vue";

const props = defineProps(["title", "rating"]);
const info = ref(props.title);
const rating = ref(parseInt(props.rating));
console.log(typeof rating.value);
// const emptyStars = ref(5 - props.rating);
console.log(info.value);
</script>

<template>
  <v-row class="pl-7 pr-15" no-gutters justify="space-between" align="center">
    <p class="text-start description-text">{{ info }}</p>
    <div>
      <v-row no-gutters dense>
        <v-icon size="13" v-for="index in rating" :key="index" color="yellow">
          mdi-star
        </v-icon>
        <v-icon size="13" v-for="index in 5 - rating" :key="index" color="grey">
          mdi-star
        </v-icon>
      </v-row>
    </div>
  </v-row>
</template>

<style>
.grey-color {
  color: #858585;
}
</style>
