<template>
  <ion-page>
    <ion-content :fullscreen="true">
      <ion-header collapse="condense">
        <ion-toolbar>
          <ion-title class="main-title" size="large">Ready ?</ion-title>
        </ion-toolbar>
      </ion-header>

      <p class="start-game" @click="takePhoto()">Go</p>
      <ion-grid>
        <ion-row>
          <ion-col size="6" :key="photo" v-for="photo in photos">
            <ion-img :src="photo.webviewPath"></ion-img>
            <p>{{photo.webviewPath}}</p>
          </ion-col>
        </ion-row>
      </ion-grid>
      <ChronoView />
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
import { usePhotoGallery, UserPhoto } from "@/composables/usePhotoGallery";
import ChronoView from "@/composents/ChronoView.vue";
import { useStopwatch } from "vue-timer-hook";

export default defineComponent({
  name: "HomePage",
  components: {
    IonContent,
    IonHeader,
    IonPage,
    IonTitle,
    IonToolbar,
    ChronoView,
  },
  setup() {
    const { photos, takePhoto } = usePhotoGallery();

    return {
      photos,
      takePhoto,
      openLibrary() {
        alert("open lib");
      },
      switchCamera() {
        alert("switch");
      },
    };
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
