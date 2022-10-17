<script setup>
import { ref, defineProps } from "vue";

const props = defineProps(["title", "iconPath"]);
const title = ref(props.title);
// const iconPath = ref("@/assets/images/softwares/" + props.iconPath);
const onHoverStyleObject = ref({
  backgroundImage: `url(${require("@/assets/images/softwares/" +
    props.iconPath)})`,
  backgroundSize: "cover",
});
</script>

<template>
  <v-row class="pl-2" no-gutters align="center">
    <div class="software-icon-size" :style="onHoverStyleObject"></div>
    <p class="text-start description-text ml-10">{{ title }}</p>
  </v-row>
</template>

<style>
.grey-color {
  color: #858585;
}
.software-icon-size {
  width: 26px;
  height: 26px;
}
</style>
