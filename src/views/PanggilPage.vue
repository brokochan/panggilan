<template>
    <ion-content :fullscreen="true" class="ion-padding">
        <ion-grid class="text-center">
            <p>Terenkripsi secara end-to-end</p>
            <img src="/assets/img/gue.jpg" class="profil"> 
            <br>
            <br>
            <b>Negova Julyan Herman</b> <br>
            <div class="sub-nama">
                NIM : 041697321 <br>
                UPBJJ : Purwokerto <br>
            </div>
            <br>
            <div class="status">
                Berdering
            </div>
        </ion-grid>
    </ion-content>
    <ion-footer>
        <ion-toolbar>
            <ion-grid>
                <ion-row>
                    <ion-col class="text-center">
                        <ion-icon :icon="volumeHigh" class="iconToolbar"></ion-icon>
                    </ion-col>
                    <ion-col class="text-center">
                        <ion-icon :icon="videocam" class="iconToolbar"></ion-icon>
                    </ion-col>
                    <ion-col class="text-center">
                        <ion-icon :icon="micOff" class="iconToolbar"></ion-icon>
                    </ion-col>
                    <ion-col class="text-center">
                        <ion-nav-link router-direction="forward" :component="goToTelepon">
                            <ion-icon :icon="closeCircle" class="iconToolbar close"></ion-icon>
                        </ion-nav-link>
                    </ion-col>
                </ion-row>
            </ion-grid>
        </ion-toolbar>
    </ion-footer>
</template>

<script>
import { defineComponent } from 'vue';
import { IonContent, IonButton, IonNavLink, IonIcon, IonFooter, IonToolbar } from '@ionic/vue';
import { volumeHigh, videocam, micOff, closeCircle } from 'ionicons/icons';
import Telepon from './TeleponPage.vue';

export default defineComponent({
    name: 'TeleponPage',
    component: {
        IonContent,
        IonButton,
        IonIcon,
        IonFooter,
        IonToolbar,
        volumeHigh, videocam, micOff, closeCircle,
    },
    data() {
        return {
            volumeHigh, videocam, micOff, closeCircle,
            goToTelepon: Telepon
        }
    }
});
</script>

<style>
.text-center {
    text-align: center;
}
.iconToolbar {
    font-size: 25px;
}
.close {
    color: red;
    font-size: 28px !important;
}
.profil {
    text-align: center;
    border-radius: 50%;
    width: 150px;
}
.sub-nama {
    font-size: 13px;
}
.status {
    color: rgb(85, 83, 83);
}
</style>