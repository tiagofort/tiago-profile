<template>
    <v-container  fill-height fluid class="transparent">
        <v-layout align-start justify-center>
            <v-card width="900" class="rounded-xl text-center" color="#000000">
                <v-card-title class="text-h4">Skills</v-card-title>
                <div class="text-h5 px-0 hidden-xs-only text-center mb-5">Languages</div>
                <div class="text-h6 px-0 hidden-sm-and-up text-center mb-5">Languages</div>
                <v-row align="center" justify="center">
                    <v-col xs="6" sm="6" md="3" lg="3" xl="3" class="px-0 ml-2">
                        <Badge text="JavaScript" icon="mdi-language-javascript" setcolor="#323330"/>
                    </v-col>
                    <v-col xs="6" sm="6" md="3" lg="3" xl="3" class="px-0 ml-2">
                        <Badge text="TypeScript" icon="mdi-language-typescript" setcolor="#2d79c7" />
                    </v-col>
                    <v-col xs="6" sm="6" md="3" lg="3" xl="3" class="px-0 ml-2">
                        <Badge text="NodeJS" icon="mdi-nodejs" setcolor="#80bd01" />
                    </v-col>
                    <v-col xs="6" sm="6" md="3" lg="3" xl="3" class="px-0 ml-2">
                        <Badge text="JAVA" icon="mdi-language-java" setcolor="#5382a1" />
                    </v-col>
                    <v-col xs="6" sm="6" md="3" lg="3" xl="3" class="px-0 ml-2">
                        <Badge text="HTML5" icon="mdi-language-html5" setcolor="#e34f26" />
                    </v-col>
                    <v-col xs="6" sm="6" md="3" lg="3" xl="3" class="px-0 ml-2">
                        <Badge text="CSS3" icon="mdi-language-css3" setcolor="#1572b6" />
                    </v-col>
                </v-row>
                <div class="text-h5 px-0 hidden-xs-only mt-5 text-center mb-5">Frameworks & Libraries</div>
                <div class="text-h6 px-0 hidden-sm-and-up mt-5 text-center mb-5">Frameworks & Libraries</div>
                <v-row align="center" justify="center">
                    <v-col xs="6" sm="6" md="3" lg="3" xl="3" class="px-0 ml-2">
                        <Badge text="VueJS" icon="mdi-vuejs" setcolor="#00c180" />
                    </v-col>
                    <v-col xs="6" sm="6" md="3" lg="3" xl="3" class="px-0 ml-2">
                        <Badge text="Nuxt" icon="mdi-nuxt" setcolor="#00dc82" />
                    </v-col>
                    <v-col xs="6" sm="6" md="3" lg="3" xl="3" class="px-0 ml-2">
                        <Badge text="Vuetify" icon="mdi-vuetify" setcolor="#1697f6" />
                    </v-col>
                    <v-col xs="6" sm="6" md="3" lg="3" xl="3" class="px-0 ml-2">
                        <Badge text="Bootstrap" icon="mdi-bootstrap" setcolor="#1697f6" />
                    </v-col>
                    <v-col xs="6" sm="6" md="3" lg="3" xl="3" class="px-0 ml-2">
                        <Badge text="React" icon="mdi-react" setcolor="#1697f6" />
                    </v-col>
                    <v-col xs="6" sm="6" md="3" lg="3" xl="3" class="px-0 ml-2">
                        <Badge text="Sass" icon="mdi-sass" setcolor="#1697f6" />
                    </v-col>
                </v-row>
                <div class="text-h5 px-0 hidden-xs-only mt-5 text-center mb-5">Other Tools</div>
                <div class="text-h6 px-0 hidden-sm-and-up mt-5 text-center mb-5">Other Tools</div>
                <v-row align="center" justify="center">
                    <v-col xs="6" sm="6" md="3" lg="3" xl="3" class="px-0 ml-2">
                        <Badge text="MongoDB" icon="mdi-code-braces" setcolor="#439945" />
                    </v-col>
                    <v-col xs="6" sm="6" md="3" lg="3" xl="3" class="px-0 ml-2">
                        <Badge text="MYSQL" icon="mdi-database" setcolor="#e48e00" />
                    </v-col>
                    <v-col xs="6" sm="6" md="3" lg="3" xl="3" class="px-0 ml-2">
                        <Badge text="Postgresql" icon="mdi-elephant" setcolor="#316092" />
                    </v-col>
                    <v-col xs="6" sm="6" md="3" lg="3" xl="3" class="px-0 ml-2">
                        <Badge text="AWS" icon="mdi-aws" setcolor="#203344" />
                    </v-col>
                    <v-col xs="6" sm="6" md="3" lg="3" xl="3" class="px-0 ml-2">
                        <Badge text="AWS Bucket" icon="mdi-aws" setcolor="#d64e3f" />
                    </v-col>
                    <v-col xs="6" sm="6" md="3" lg="3" xl="3" class="px-0 ml-2">
                        <Badge text="Git" icon="mdi-git" setcolor="#1697f6" />
                    </v-col>
                </v-row>
            </v-card>    
        </v-layout>
    </v-container>
</template>

<script>
import Badge from '@/components/Badge.vue';
export default {
    data () {
        return {
        } 
    },
    components: { Badge } 
}
</script>
