<template>
    <v-container  fill-height fluid class="transparent">
        <v-layout align-start justify-center>
                <v-card width="900" class="rounded-xl" color="#000000">
                    <v-card-title class="text-h4 px-0 hidden-sm-and-down">Projects</v-card-title>
                    <v-card-title class="text-h6 px-0 hidden-sm-and-up">Projects</v-card-title>
                    <v-row
                        class="fill-height text-left"
                        align="center"
                        justify="center"
                    >
                        <template v-for="(item, i) in paginatedItems">
                            <v-col
                                :key="i"
                                cols="12"
                                md="4"
                            >
                                <v-hover v-slot="{ hover }">
                                    <v-card
                                        :elevation="hover ? 12 : 2"
                                        :class="{ 'on-hover': hover }"
                                        color="white"
                                        class="pa-1"
                                    >
                                        <v-img
                                            contain
                                            :src="item.img"
                                            height="200"
                                        >
                                            <v-expand-transition>
                                                <div
                                                    v-if="hover"
                                                    class="d-flex transition-fast-in-fast-out grey darken-3 v-card--reveal text-h2 white--text"
                                                    style="height: 100%;"
                                                >
                                                    <v-card-text>
                                                        <v-row
                                                            class="fill-height flex-column"
                                                            justify="space-between"
                                                        >
                                                            <p class="mt-2 subheading text-center white--text">
                                                                {{ item.title }}
                                                            </p>
                                                            <p class="caption text-center white--text">
                                                                {{ item.resume }}
                                                            </p>
                                                            <div class="align-self-center">
                                                                <v-btn
                                                                        class="my-button"
                                                                        color="white"
                                                                        icon
                                                                        x-large
                                                                        @click="openLink(item.git)"
                                                                >
                                                                    <v-icon
                                                                        class="show-btns"
                                                                        :color="transparent"
                                                                        x-large
                                                                    >
                                                                        {{ item.git_icon }}
                                                                    </v-icon>
                                                                </v-btn>
                                                                <v-btn
                                                                        class="my-button"
                                                                        color="white"
                                                                        icon
                                                                        x-large
                                                                        @click="openLink(item.site)"
                                                                >
                                                                    <v-icon
                                                                        class="show-btns"
                                                                        :color="transparent"
                                                                        x-large
                                                                    >
                                                                        {{ item.site_icon }}
                                                                    </v-icon>
                                                                </v-btn>
                                                            </div>
                                                        </v-row>
                                                    </v-card-text>
                                                </div>
                                            </v-expand-transition> 
                                        </v-img>
                                    </v-card>
                                </v-hover>
                            </v-col>
                        </template>
                    </v-row>
                    <v-row justify="center" align="center" class="mt-3 mr-2 ml-2">
                        <v-pagination
                            color="#000000"
                            v-model="currentPage"
                            :length="totalPages"
                            @input="updatePage"
                            circle
                            light
                        ></v-pagination>
                    </v-row>
                </v-card>
        </v-layout>
    </v-container>
</template>

<script>
import lunalogo from '@/static/projects/logoLuna.svg';
import tiagoprof from '@/static/projects/tiago-profile.png';
export default {
    data () {
        return {
            currentPage: 1,
            itemsPerPage: 3,
            items: 
            [
                {
                    title: 'Tiago Profile',
                    resume: 'My professional page',
                    git_icon: 'mdi-git', 
                    git: 'https://github.com/tiagofort/tiago-profile',
                    site_icon: 'mdi-share', 
                    site: 'https://tiago-profile-35060e7961af.herokuapp.com/',
                    img: tiagoprof
                },
                {
                    title: 'Luna Crystals API',
                    resume: 'Luna Crystals API developed in NodeJs',
                    git_icon: 'mdi-git', 
                    git: 'https://github.com/tiagofort/luna-crystals-API',
                    site_icon: 'mdi-share', 
                    site: '',
                    img: lunalogo
                },
            ],
            transparent: 'rgba(44, 40, 24, 0.43)'
        } 
    },
    methods:{
        openLink(url){
            window.open(url, '_blank');
        },
        updatePage(page) {
            this.currentPage = page;
        },
    },
    computed:{
        totalPages() {
            return Math.ceil(this.items.length / this.itemsPerPage);
        },
        paginatedItems() {
            const startIndex = (this.currentPage - 1) * this.itemsPerPage;
            const endIndex = startIndex + this.itemsPerPage;
            return this.items.slice(startIndex, endIndex);
        },   
    },
}
</script>

<style scoped>
.show-btns {
  color: rgb(250, 248, 248) !important;
}

.v-card--reveal {
  align-items: center;
  bottom: 0;
  justify-content: center;
  opacity: 1.5;
  position: absolute;
  width: 100%;
}
</style>