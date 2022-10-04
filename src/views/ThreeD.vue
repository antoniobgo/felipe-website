<script setup>
import PortfolioCard from "@/components/PortfolioCard.vue";

const portfolioItems = [
  {
    jobName: "HELMET GRAPHICS",
    jobCompany: "Illustration and Render",
    softwareText: "Software: Blender and Illustrator",
    backgroundUrl: "threed/helmet_graphics.png",
  },
  {
    jobName: "MORMAII HELMET",
    jobCompany: "Modeling, Render and Animation",
    softwareText: "Software: Blender and Illustrator",
    backgroundUrl: "threed/mormaii.png",
  },
  {
    jobName: "Fruit candy packaging 3d",
    jobCompany: "Modeling, Render and Animation",
    softwareText: "Softwares: Blender",
    backgroundUrl: "threed/primor.png",
  },
  {
    jobName: "PET BOTTLE",
    jobCompany: "Modeling and Render",
    softwareText: "Softwares: Blender and Photoshop",
    backgroundUrl: "threed/bottle.png",
  },
  {
    jobName: "STAR HUNTER LOGO",
    jobCompany: "Modeling, Render and Layout",
    softwareText: "Softwares: Blender and Unreal",
    backgroundUrl: "threed/starhunter.png",
  },
  {
    jobName: "LOWPOLY PACK",
    jobCompany: "Modeling, Render and Animation",
    softwareText: "Software: Blender",
    backgroundUrl: "threed/lowpoly.png",
  },
  {
    jobName: "INSPIRED BY MEDICINE",
    jobCompany: "Modeling, Render and Animation",
    softwareText: "Softwares: Blender",
    backgroundUrl: "threed/inspired.png",
  },
  {
    jobName: "ADVERTISING CAMPAIGN",
    jobCompany: "Oliveira Imóveis",
    softwareText: "Softwares: After Effects and Illustrator",
    backgroundUrl: "threed/oliveira.png",
  },
  {
    jobName: "NARRATIVA INSPIRA MOVIMENTAR",
    jobCompany: "Autoral",
    softwareText: "Softwares: Illustrator, Photoshop and After Effects",
    backgroundUrl: "threed/capa_motion.png",
  },
  {
    jobName: "MOTION EVENT",
    jobCompany: "Creative Led",
    softwareText: "Softwares: Illustrator and After Effects",
    backgroundUrl: "threed/duelo.png",
  },
  {
    jobName: "MOTION AND VISUAL IDENTITY",
    jobCompany: "Essência don Campo",
    softwareText: "Softwares: Illustrator, Photoshop and After Effects",
    backgroundUrl: "threed/essencia_do_campo.png",
  },
  {
    jobName: "MOTION LOGO",
    jobCompany: "Rosane Dutra",
    softwareText: "Softwares: After Effects",
    backgroundUrl: "threed/rosane.png",
  },
];
</script>

<template>
  <div class="motion">
    <v-row justify="center" class="threed-container" no-gutters dense>
      <v-col cols="9">
        <v-row no-gutters dense justify="center">
          <v-col cols="8">
            <v-row no-gutters dense justify="start">
              <p class="title-text">3D</p>
            </v-row>
            <v-row>
              <v-col cols="4">
                <PortfolioCard :job="portfolioItems[0]" :cardHeight="444" />
              </v-col>
              <v-col cols="8">
                <PortfolioCard :job="portfolioItems[1]" :cardHeight="444" />
              </v-col>
            </v-row>
            <v-row>
              <v-col cols="8">
                <PortfolioCard :job="portfolioItems[2]" :cardHeight="310" />
              </v-col>
              <v-col cols="4">
                <PortfolioCard :job="portfolioItems[3]" :cardHeight="310" />
              </v-col>
            </v-row>
            <v-row>
              <v-col cols="4">
                <PortfolioCard :job="portfolioItems[4]" :cardHeight="445" />
              </v-col>
              <v-col cols="4">
                <PortfolioCard :job="portfolioItems[5]" :cardHeight="445" />
              </v-col>
              <v-col cols="4">
                <PortfolioCard :job="portfolioItems[6]" :cardHeight="445" />
              </v-col>
            </v-row>
          </v-col>
        </v-row>
      </v-col>
    </v-row>
  </div>
</template>

<style scoped>
.motion {
  background-color: #101010;
  width: 100%;
  height: 100%;
}
.threed-container {
  padding-top: 5rem;
  margin-bottom: 10rem;
}
.title-text {
  font-family: Alata, sans-serif;
  font-size: 1.5rem;
  color: #c8c8c8;
  letter-spacing: 1rem;
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
  min-height: 19.3rem;
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
