<template>
  <ion-page>
    <ion-content :fullscreen="true">
      <ion-header collapse="condense">
        <ion-toolbar class="header-wrapper">
          <ion-title class="main-title" size="large">Nope</ion-title>
        </ion-toolbar>
        <p class="timer">12.43.567</p>
      </ion-header>

      <div class="image-wrapper">
        <img class="image-inner" src="" alt="" />
      </div>

      <div class="button-wrapper">
        <a href="/home" class="give-up">Give up</a>
        <a href="/camera" class="back-game">Back in game</a>
      </div>
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
  name: "NopeView",
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
.main-title {
  color: #ff0005;
}

.timer {
  margin: 0;
  padding: 2.415vw;
  text-align: center;
  background-color: #fff;
  border-radius: 0 0 10.87vw 10.87vw;
}

.button-wrapper {
  margin: 5.556vw;
  display: flex;
  justify-content: center;
  align-items: center;
  gap: 9.662vw;
}

.give-up,
.back-game {
  width: 21.498vw;
  height: 21.498vw;
  font-size: 3.382vw;
  line-height: 90%;
}

.give-up {
  background-color: #ff0005;
  color: #fff;
}

.back-game {
  background-color: #ffc409;
  color: #000;
}
</style>
