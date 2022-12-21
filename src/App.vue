<template>
  <ion-nav :root="component"></ion-nav>
</template>

<script lang="ts">
import { defineComponent } from 'vue';
import { IonNav } from '@ionic/vue';
import HomePage from './views/HomePage.vue';

export default defineComponent({
  name: 'App',
  components: {
    IonNav
  },
  setup () {
    return {
      component: HomePage
    }
  }
});
</script>