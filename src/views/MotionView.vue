<script setup>
import PortfolioCard from "@/components/PortfolioCard.vue";

const portfolioItems = [
  {
    jobName: "MOTION HUD",
    jobCompany: "Agência 300",
    softwareText: "Software: After Effects",
    backgroundUrl: "motion_hud.png",
  },
  {
    jobName: "RUNNING CYCLES",
    jobCompany: "Autoral test character animation",
    softwareText: "Software: After Effects",
    backgroundUrl: "running.png",
  },
  {
    jobName: "APPS LAUNCH CAMPAIGN",
    jobCompany: "Hughueir APS",
    softwareText:
      "Softwares: After Effects, Premiere, Photoshop and Illustrator",
    backgroundUrl: "launch_app.png",
  },
  {
    jobName: "WAKE UP",
    jobCompany: "Illustration and Animation Authorial",
    softwareText: "Softwares: After Effects, Premiere and Illustrator",
    backgroundUrl: "wakeup.png",
  },
  {
    jobName: "PRICE OFFERS VIDEO",
    jobCompany: "Led Outdoor",
    softwareText: "Softwares: C4D, After Effects",
    backgroundUrl: "imperatriz.png",
  },
  {
    jobName: "PRE-LAUNCH VIDEO MARFARÁ",
    jobCompany: "Agencia 300",
    softwareText: "Software: After Effects",
    backgroundUrl: "marfara.png",
  },
  {
    jobName: "SCRIPT, EDITION AND MOTION",
    jobCompany: "Plaza Jardim",
    softwareText: "Softwares: Premiere and After Effects",
    backgroundUrl: "plaza.png",
  },
  {
    jobName: "ADVERTISING CAMPAIGN",
    jobCompany: "Oliveira Imóveis",
    softwareText: "Softwares: After Effects and Illustrator",
    backgroundUrl: "oliveira.png",
  },
  {
    jobName: "NARRATIVA INSPIRA MOVIMENTAR",
    jobCompany: "Autoral",
    softwareText: "Softwares: Illustrator, Photoshop and After Effects",
    backgroundUrl: "capa_motion.png",
  },
  {
    jobName: "MOTION EVENT",
    jobCompany: "Creative Led",
    softwareText: "Softwares: Illustrator and After Effects",
    backgroundUrl: "duelo.png",
  },
  {
    jobName: "MOTION AND VISUAL IDENTITY",
    jobCompany: "Essência don Campo",
    softwareText: "Softwares: Illustrator, Photoshop and After Effects",
    backgroundUrl: "essencia_do_campo.png",
  },
  {
    jobName: "MOTION LOGO",
    jobCompany: "Rosane Dutra",
    softwareText: "Softwares: After Effects",
    backgroundUrl: "rosane.png",
  },
];
</script>

<template>
  <div class="motion">
    <v-row justify="center" class="motion-container" no-gutters dense>
      <v-col cols="9">
        <v-row no-gutters dense justify="center">
          <v-col cols="8">
            <v-row no-gutters dense justify="start">
              <p class="title-text">MOTION</p>
            </v-row>
            <v-row>
              <v-col cols="8">
                <PortfolioCard :job="portfolioItems[0]" :cardHeight="310" />
              </v-col>
              <v-col cols="4">
                <PortfolioCard :job="portfolioItems[1]" :cardHeight="310" />
              </v-col>
            </v-row>
            <v-row>
              <v-col cols="4">
                <PortfolioCard :job="portfolioItems[2]" :cardHeight="444" />
              </v-col>
              <v-col cols="8">
                <PortfolioCard :job="portfolioItems[3]" :cardHeight="444" />
              </v-col>
            </v-row>
            <v-row>
              <v-col cols="4">
                <PortfolioCard :job="portfolioItems[4]" :cardHeight="310" />
              </v-col>
              <v-col cols="4">
                <PortfolioCard :job="portfolioItems[5]" :cardHeight="310" />
              </v-col>
              <v-col cols="4">
                <PortfolioCard :job="portfolioItems[6]" :cardHeight="310" />
              </v-col>
            </v-row>
            <v-row>
              <v-col cols="4">
                <PortfolioCard :job="portfolioItems[7]" :cardHeight="310" />
              </v-col>
              <v-col cols="8">
                <PortfolioCard :job="portfolioItems[8]" :cardHeight="310" />
              </v-col>
              <v-row>
                <v-col cols="4">
                  <PortfolioCard :job="portfolioItems[9]" :cardHeight="310" />
                </v-col>
                <v-col cols="4">
                  <PortfolioCard :job="portfolioItems[10]" :cardHeight="310" />
                </v-col>
                <v-col cols="4">
                  <PortfolioCard :job="portfolioItems[11]" :cardHeight="310" />
                </v-col>
              </v-row>
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
.motion-container {
  padding-top: 5rem;
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
