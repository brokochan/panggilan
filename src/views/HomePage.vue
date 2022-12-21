<template>
  <ion-page>
    <ion-header :translucent="true">
      <ion-toolbar class="text-center">
        <ion-title>Aplikasi Telepon By NEGOVA</ion-title>
      </ion-toolbar>
    </ion-header>
    
    <ion-content :fullscreen="true">
      <ion-header collapse="condense">
        <ion-toolbar>
          <ion-title size="large">Blank</ion-title>
        </ion-toolbar>
      </ion-header>
    
      <div id="container">
        <ion-nav-link router-direction="forward" :component="goToTelepon">
          <ion-button>Telepon</ion-button>
        </ion-nav-link>
      </div>
    </ion-content>
  </ion-page>
</template>

<script lang="ts">
import { IonContent, IonHeader, IonPage, IonTitle, IonToolbar, IonButton, IonNavLink } from '@ionic/vue';
import { defineComponent } from 'vue';
import Telepon from './TeleponPage.vue';

export default defineComponent({
  name: 'HomePage',
  components: {
    IonContent,
    IonHeader,
    IonPage,
    IonTitle,
    IonToolbar,
    IonButton,
    IonNavLink
  },
  setup () {
    return { goToTelepon: Telepon }
  }
});
</script>

<style scoped>
.text-center {
    text-align: center;
}
#container {
  text-align: center;
  
  position: absolute;
  left: 0;
  right: 0;
  top: 50%;
  transform: translateY(-50%);
}

#container strong {
  font-size: 20px;
  line-height: 26px;
}

#container p {
  font-size: 16px;
  line-height: 22px;
  
  color: #8c8c8c;
  
  margin: 0;
}

#container a {
  text-decoration: none;
}
</style>
