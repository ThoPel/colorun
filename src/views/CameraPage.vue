<template>
  <ion-page>
    <ion-content>
      <camera
        :width="200"
        :height="200"
        :requestAccess="true"
        @camera:captured="getImage"
      >
        <div slot="capture" name="capture">snap</div>
        <div slot="download" name="download">save</div>
      </camera>
      <p>yo</p>
    </ion-content>
  </ion-page>
</template>

<script>
import { defineComponent } from "vue";
import { Camera } from "vue-capture";
import { IonContent, IonPage } from '@ionic/vue';

export default defineComponent({
  components: { Camera, IonContent, IonPage  },
  methods: {
    getImage(data) {
      // 'data' is the image captured in base64 format
    },
  },
});
</script>

<style scoped></style>
