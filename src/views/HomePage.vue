<template>
  <ion-page>
    <ion-content :fullscreen="true">
      <ion-header collapse="condense">
        <ion-toolbar>
          <ion-title class="main-title" size="large">Ready ?</ion-title>
        </ion-toolbar>
      </ion-header>

      <p class="start-game">Go</p>
    </ion-content>
  </ion-page>
</template>

<script lang="ts">
import {
  IonContent,
  IonHeader,
  IonPage,
  IonTitle,
  IonToolbar,
} from "@ionic/vue";
import { defineComponent } from "vue";

export default defineComponent({
  name: "HomePage",
  components: {
    IonContent,
    IonHeader,
    IonPage,
    IonTitle,
    IonToolbar,
  },
});
</script>

<style scoped>
.main-title,
.start-game {
  font-family: "Kinetic", sans-serif;
  text-transform: uppercase;
  font-weight: 900;
  text-align: center;
}

.start-game {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  width: 72.464vw;
  height: 72.464vw;
  background-color: #ffc409;
  font-size: 15.459vw;
}
</style>
