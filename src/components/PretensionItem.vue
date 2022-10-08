<script setup>
import { ref, defineProps } from "vue";

const props = defineProps(["title"]);
const title = ref(props.title);
</script>

<template>
  <v-row no-gutters dense>
    <v-btn class="rounded-lg pretension-container">
      <p class="pretension-text">
        {{ title }}
      </p>
    </v-btn>
  </v-row>
  <!-- <v-btn class="rounded-pill pretension-container">
    <v-row justify="center" dense no-gutters align="center" class="h-100">
      <v-col>
        <p class="pretension-text">
          {{ title }}
        </p>
      </v-col>
    </v-row>
  </v-btn> -->
</template>

<style scoped>
.pretension-container {
  background-color: #1e1e1e;
  height: 29px;
  min-width: 112px;
}
.pretension-text {
  line-height: 1.208rem;
  font-size: 0.875rem;
  letter-spacing: 0.281rem;
  color: #858585;
}
</style>
