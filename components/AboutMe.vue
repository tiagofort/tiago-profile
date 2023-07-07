<template>
        <v-container  fill-height fluid class="transparent">
            <v-layout align-start justify-center>
                    <v-card width="900" class="rounded-xl hidden-sm-and-down" color="#000000">
                        <v-list-item three-line>
                            <v-list-item-content class="pa-3">
                                <v-list-item-title class="text-h2 text-md-h3 mb-1 ml-5">
                                    {{ name }}
                                </v-list-item-title>
                                <v-list-item-title class="text-h4 text-md-h5 mb-1 ml-8">
                                    {{ definition }}
                                </v-list-item-title>
                                <v-list-item-content class="text-subtitle-1 text-justify mt-10 ml-5 pa-2">
                                    {{ resume }}
                                </v-list-item-content>
                            </v-list-item-content>
                            <v-list-item-avatar size="200" class="avatar">
                                <img :src="avatar" alt="John">
                            </v-list-item-avatar>
                        </v-list-item>
                    </v-card>
                    <v-card :width="getMaxWidth" height="auto" class="hidden-md-and-up text-center" color="#000000">
                        <v-row>
                            <v-col class="pa-0 mt-5 text-center">
                                <v-avatar size="200" class="avatar">
                                    <img
                                        :src="avatar"
                                    >
                                </v-avatar>
                            </v-col>
                        </v-row>
                        <v-row>
                            <v-col class="pa-0 pb-1 mt-3 text-center">
                                <div class="text-center text-h4">{{ name }}</div><br>
                                <div class="text-center text-h6 mt-n2">{{ definition }}</div><br>
                            </v-col>
                        </v-row>
                        <v-row>
                            <v-col>
                                <div class="text-subtitle-1 text-justify pa-2">{{ resume }}</div><br>
                            </v-col>
                        </v-row>
                    </v-card>
            </v-layout>
        </v-container>
</template>

<script>
import avatar from '@/static/avatar/avatar2.png';
export default{
    data: () => ({ 
        avatar: avatar,
        maxWidth: 0,
        name: 'Tiago Fortaleza Gai',
        definition: 'Full Stack Developer',
        resume: 'This page was developed with the intention of sharing a little of my professional experience,' +
                ' my main skills and projects. I have a degree in Information Systems and a postgraduate degree in' + 
                ' web development. I have about eight years of experience as a programmer, using mainly Java and'+
                ' JavaScript as main languages. Currently I am only focused on JavaScript projects,' +
                ' but I am always open and willing to new challenges. A new technology is nothing more'+
                ' than a new opportunity to keep learning and evolving. I would like to point out that I leave here a brief' +
                ' and superficial summary of who I am as a person and as a professional. This is just the cover of the book, so please' + 
                ' don not judge my professional life book by its cover. Would be a pleasure to be able to' +
                ' share in more detail who I am after opening the book.'

    }),
    computed:{
      getMaxWidth(){
        return this.$vuetify.breakpoint.width - (this.$vuetify.breakpoint.width * 0.1);
      }  
    }
}
</script>

<style>
.transparent {
    background-color: transparent;
}
.avatar {
    width: 100px;
    height: 100px;
}
  
.avatar img {
    object-fit: cover;
    width: 100%;
    height: 100%;
}
</style>