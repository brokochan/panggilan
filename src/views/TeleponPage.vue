<template>
    <ion-content :fullscreen="true" class="ion-padding">
        <ion-grid style="height:100%">
            <ion-row style="height:50%">
                <ion-col>
                    <ion-searchbar placeholder="Cari disini..."></ion-searchbar>
                    <ion-list>
                        <ion-item>
                            <ion-grid>
                                <ion-row>
                                    <ion-col size="3" class="text-center">
                                        <ion-icon :icon="personCircleOutline" class="iconPerson"></ion-icon>
                                    </ion-col>
                                    <ion-col size="8">
                                        <div class="nama">
                                            Pak Ripa DPMPT (2)
                                        </div>
                                        <div class="sub-nama">
                                            +87987979878 Indonesia 12:23
                                        </div>
                                    </ion-col>
                                </ion-row>
                            </ion-grid>
                        </ion-item>
                        <ion-item>
                            <ion-grid>
                                <ion-row>
                                    <ion-col size="3" class="text-center">
                                        <ion-icon :icon="personCircleOutline" class="iconPerson"></ion-icon>
                                    </ion-col>
                                    <ion-col size="8">
                                        <div class="nama">
                                            Pak Aji DPMPT (2)
                                        </div>
                                        <div class="sub-nama">
                                            +87987979878 Indonesia 12:23
                                        </div>
                                    </ion-col>
                                </ion-row>
                            </ion-grid>
                        </ion-item>
                        <ion-item>
                            <ion-grid>
                                <ion-row>
                                    <ion-col size="3" class="text-center">
                                        <ion-icon :icon="personCircleOutline" class="iconPerson"></ion-icon>
                                    </ion-col>
                                    <ion-col size="8">
                                        <div class="nama">
                                            Pak Ganjar DPMPT (2)
                                        </div>
                                        <div class="sub-nama">
                                            +87987979878 Indonesia 12:23
                                        </div>
                                    </ion-col>
                                </ion-row>
                            </ion-grid>
                        </ion-item>
                    </ion-list>
                </ion-col>
            </ion-row>
            <ion-row style="height:50%">
                <ion-grid>
                    <ion-row>
                        <ion-grid>
                            <ion-row>
                                <ion-col>
                                    <ion-input class="text-center" v-model="text"
                                        style="display:inline-block;z-index: 1;position:relative;"></ion-input>
                                    <div style="display: inline-block">
                                        <ion-icon slot="icon-only" :icon="backspace" @click="hapus"
                                            style="font-size:39px;color:#428cff;vertical-align: middle;z-index:2;position:absolute;top:5px;right:5px;"></ion-icon>
                                    </div>
                                </ion-col>
                            </ion-row>
                        </ion-grid>
                    </ion-row>
                    <ion-row>
                        <ion-grid class="text-center">
                            <ion-row>
                                <ion-col>
                                    <div class="angka" @click="Click1">1</div>
                                    <div class="huruf"></div>
                                </ion-col>
                                <ion-col>
                                    <div class="angka" @click="Click2">2</div>
                                    <div class="huruf">ABC</div>
                                </ion-col>
                                <ion-col>
                                    <div class="angka" @click="Click3">3</div>
                                    <div class="huruf">DEF</div>
                                </ion-col>
                            </ion-row>
                            <ion-row>
                                <ion-col>
                                    <div class="angka" @click="Click4">4</div>
                                    <div class="huruf">GHI</div>
                                </ion-col>
                                <ion-col>
                                    <div class="angka" @click="Click5">5</div>
                                    <div class="huruf">JKL</div>
                                </ion-col>
                                <ion-col>
                                    <div class="angka" @click="Click6">6</div>
                                    <div class="huruf">MNO</div>
                                </ion-col>
                            </ion-row>
                            <ion-row>
                                <ion-col>
                                    <div class="angka" @click="Click7">7</div>
                                    <div class="huruf">PQRS</div>
                                </ion-col>
                                <ion-col>
                                    <div class="angka" @click="Click8">8</div>
                                    <div class="huruf">TUV</div>
                                </ion-col>
                                <ion-col>
                                    <div class="angka" @click="Click9">9</div>
                                    <div class="huruf">WXYZ</div>
                                </ion-col>
                            </ion-row>
                            <ion-row>
                                <ion-col>
                                    <div class="angkaBintang" @click="ClickBintang">*</div>
                                    <div class="huruf">,</div>
                                </ion-col>
                                <ion-col>
                                    <div class="angka" @click="Click0">0</div>
                                    <div class="huruf">+</div>
                                </ion-col>
                                <ion-col>
                                    <div class="angka" @click="ClickPagar">#</div>
                                </ion-col>
                            </ion-row>
                        </ion-grid>
                    </ion-row>
                    <ion-row>
                        <ion-col>
                            <ion-nav-link router-direction="forward" :component="goToPanggil">
                                <ion-button expand="block" shape="round">
                                    Panggil
                                </ion-button>
                            </ion-nav-link>
                        </ion-col>
                    </ion-row>
                </ion-grid>
            </ion-row>
        </ion-grid>
    </ion-content>
</template>

<script>
import { defineComponent } from 'vue';
import { IonContent, IonButton, IonSearchbar, IonItem, IonList, IonInput, IonNavLink, IonIcon } from '@ionic/vue';
import { backspace, personCircleOutline } from 'ionicons/icons';
import Panggil from './PanggilPage.vue';

export default defineComponent({
    name: 'TeleponPage',
    components: {
        IonContent,
        IonButton,
        IonSearchbar,
        IonItem,
        IonList,
        IonInput,
        IonIcon,
    },
    methods: {
        Click0() {
            this.text += 0;
            this.panjangText = this.text.length;
        },
        Click1() {
            this.text += 1;
            this.panjangText = this.text.length;
        },
        Click2() {
            this.text += 2;
            this.panjangText = this.text.length;
        },
        Click3() {
            this.text += 3;
            this.panjangText = this.text.length;
        },
        Click4() {
            this.text += 4;
            this.panjangText = this.text.length;
        },
        Click5() {
            this.text += 5;
            this.panjangText = this.text.length;
        },
        Click6() {
            this.text += 6;
            this.panjangText = this.text.length;
        },
        Click7() {
            this.text += 7;
            this.panjangText = this.text.length;
        },
        Click8() {
            this.text += 8;
            this.panjangText = this.text.length;
        },
        Click9() {
            this.text += 9;
            this.panjangText = this.text.length;
        },
        ClickBintang() {
            this.text += '*';
            this.panjangText = this.text.length;
        },
        ClickPagar() {
            this.text += '#';
            this.panjangText = this.text.length;
        },
        hapus() {
            this.panjangText = this.text.length;
            if (this.panjangText > 0) {
                this.text = this.text.substring(this.panjangText - 1, -1);
            } else {
                this.panjangText = 0;
                this.text = '';
            }
        }
    },
    data() {
        return {
            text: '',
            panjangText: 0,
            backspace,
            personCircleOutline,
            goToPanggil: Panggil
        };
    }
});
</script>

<style scoped>
ion-button {
    text-transform: none;
}

.text-center {
    text-align: center;
}

.angka {
    font-size: 24px;
}

.angkaBintang {
    font-size: 35px;
    margin-bottom: -32px;
}

.huruf {
    font-size: 10px;
}
.iconPerson {
    font-size: 40px;
}
.nama {
    margin-top: 4px;
    font-weight: bold;
}
.sub-nama {
    font-size: 13px;
}

/* rippe efect */
.ripple-parent {
  display: flex;
  align-items: center;
  justify-content: center;

  position: relative;
  overflow: hidden;

  background-color: #428cff;

  user-select: none;

  width: 100%;
  height: 50px;
  border-radius: 25px;
  cursor: pointer;
}

.custom-parent {
  color: white;
}

</style>