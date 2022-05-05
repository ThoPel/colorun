<template>
  <ion-app>
    <ion-router-outlet />
  </ion-app>
</template>

<script lang="ts">
import { IonApp, IonRouterOutlet } from "@ionic/vue";
import { defineComponent } from "vue";

export default defineComponent({
  name: "App",
  components: {
    IonApp,
    IonRouterOutlet,
  },
});
</script>

<style>
@font-face {
  font-family: "Kinetic";
  src: url("../public/assets/fonts/KineticBlack.eot");
  src: url("../public/assets/fonts/KineticBlack.eot?#iefix")
      format("embedded-opentype"),
    url("../public/assets/fonts/KineticBlack.woff2") format("woff2"),
    url("../public/assets/fonts/KineticBlack.woff") format("woff"),
    url("../public/assets/fonts/KineticBlack.ttf") format("truetype"),
    url("../public/assets/fonts/KineticBlack.svg#KineticBlack") format("svg");
  font-weight: 900;
  font-style: normal;
  font-display: swap;
}

@font-face {
  font-family: "Kinetic";
  src: url("../public/assets/fonts/KineticBold.eot");
  src: url("../public/assets/fonts/KineticBold.eot?#iefix")
      format("embedded-opentype"),
    url("../public/assets/fonts/KineticBold.woff2") format("woff2"),
    url("../public/assets/fonts/KineticBold.woff") format("woff"),
    url("../public/assets/fonts/KineticBold.ttf") format("truetype"),
    url("../public/assets/fonts/KineticBold.svg#KineticBold") format("svg");
  font-weight: bold;
  font-style: normal;
  font-display: swap;
}

a {
  text-decoration: none;
}

.main-title,
.start-game,
.timer,
.give-up,
.back-game {
  font-family: "Kinetic", sans-serif;
  text-transform: uppercase;
  font-weight: 900;
  text-align: center;
}

.main-title {
  margin: 4.831vw 0;
  height: fit-content;
}

.image-wrapper {
  width: 81.159vw;
  height: 140.58vw;
  margin: 5.556vw auto 0;
}

.image-inner {
  width: 100%;
  height: 100%;
  object-fit: cover;
}

.start-game,
.give-up,
.back-game {
  border-radius: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
}
</style>