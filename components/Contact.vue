<template>
    <v-container  fill-height fluid class="transparent">
        <v-layout align-start justify-center>
                <v-sheet width="900" class="rounded-xl hidden-xs-only transparent">
                   <v-card-title class="text-h3">Get in touch</v-card-title>
                   <v-row> 
                        <v-list-item three-line class="transparent">
                            <v-col>
                                <v-btn
                                    color="white"
                                    icon
                                    x-large 
                                    @click="getTouch('https://www.linkedin.com/in/tiago-fortaleza-gai/')"                                   
                                >
                                    <v-icon
                                        x-large
                                    >
                                        mdi-linkedin
                                    </v-icon>
                                </v-btn>
                            </v-col>
                            <v-col>
                                <v-btn
                                    color="white"
                                    icon
                                    x-large
                                    @click="getTouch('https://github.com/tiagofort')"                                    
                                >
                                    <v-icon
                                        x-large
                                    >
                                        mdi-git
                                    </v-icon>
                                </v-btn>
                            </v-col>
                            <v-col>
                                <v-btn
                                    color="white"
                                    icon
                                    x-large 
                                    @click="getTouch('https://wa.me/353830679963')"                                   
                                >
                                    <v-icon
                                        x-large
                                    >
                                        mdi-whatsapp
                                    </v-icon>
                                </v-btn>
                            </v-col>
                            <v-col>
                                <Dialog />
                            </v-col>
                            <v-col>
                                <v-list-item-avatar tile size="300" class="avatar">
                                    <img :src="img" alt="John">
                                </v-list-item-avatar>
                            </v-col>
                        </v-list-item>
                   </v-row>
                </v-sheet>
                <v-sheet :width="getMaxWidth" height="auto" class="hidden-sm-and-up text-center pa-3 transparent">
                    <v-row>
                        <v-col class="pa-0 mt-5 text-center">
                            <v-avatar tile size="200" class="avatar">
                                <img
                                    :src="img"
                                >
                            </v-avatar>
                        </v-col>
                    </v-row>
                    <v-row>
                        <v-col>
                            <div class="text-h6 text-center ">Get in touch</div>
                        </v-col>
                    </v-row>
                    <v-row>
                        <v-col>
                                <v-btn
                                    color="white"
                                    class="mr-1"
                                    icon
                                    @click="getTouch('https://www.linkedin.com/in/tiago-fortaleza-gai/')"                                        
                                >
                                    <v-icon
                                        x-large
                                    >
                                        mdi-linkedin
                                    </v-icon>
                                </v-btn>
                            </v-col>
                            <v-col>
                                <v-btn
                                    color="white"
                                    class="mr-1"
                                    icon 
                                    @click="getTouch('https://github.com/tiagofort')"                                  
                                >
                                    <v-icon
                                        x-large
                                    >
                                        mdi-git
                                    </v-icon>
                                </v-btn>
                            </v-col>
                            <v-col>
                                <v-btn
                                    color="white"
                                    class="mr-1"
                                    icon 
                                    @click="getTouch('https://wa.me/353830679963')"                                   
                                >
                                    <v-icon
                                        x-large
                                    >
                                        mdi-whatsapp
                                    </v-icon>
                                </v-btn>
                            </v-col>
                            <v-col>
                                <Dialog class="mr-1" />
                            </v-col>
                    </v-row>
                </v-sheet>
        </v-layout>
    </v-container>
</template>

<script>
import img from '@/static/contact/contact.png';
import Dialog from '@/components/Dialog.vue';
export default {
    data () {
        return {
            img: img,
        }
    },
    methods:{
      getTouch(url){
        window.open(url, '_blank');
      },  
    },
    computed:{
      getMaxWidth(){
        return this.$vuetify.breakpoint.width - (this.$vuetify.breakpoint.width * 0.1);
      }  
    },
    components:{ Dialog }
}        
</script>