<template>
    <v-app-bar app dark flat max-width="100vw">
        <v-spacer></v-spacer>
        <v-btn text  class="xs-hide white--text">
            Home
        </v-btn>
        <v-btn text href="https://blog.brandonwinger-air.com/" target="_blank" class="pl-0 pr-2 px-sm-2 px-md-4 white--text">
            Prayer
        </v-btn>
        <v-btn text  class="pl-0 pr-2 px-sm-2 px-md-4 white--text">
            Resources and trainings
        </v-btn>
        <v-btn text href="https://github.com/BrandonWingerAir" target="_blank" class="px-0 px-sm-2 px-md-4 white--text">
            Community engagements
        </v-btn>
        <!-- <v-btn text @click="scroll('about-scroll')" class="pl-0 pr-2 px-sm-2 px-md-4 black--text">
            About
        </v-btn> -->
        <v-btn text  class="px-0 px-sm-2 px-md-4 white--text">
            Events and updates
        </v-btn>
        <v-btn text  class="px-0 px-sm-2 px-md-4 white--text">
            About us
        </v-btn>
        
        <v-avatar tile size="60">
            <v-img src="/images/rick.jpg" alt="Avatar"/>
        </v-avatar>
    </v-app-bar>
</template>
