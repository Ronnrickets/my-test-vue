<template>
    <div>
        <v-row dense>
            <v-col cols="6">
                <table cellspacing="0" cellpadding="0" style="border-collapse: collapse;">
                    <tr>
                        <td class="bordertd">
                            <span class="spanletter">C</span>
                        </td>
                    </tr>
                    <tr>
                        <td class="bordertd">
                            <span class="spanletter">F</span>
                        </td>
                        <td style="margin-top: 15px;">
                            <span class="spanintercession">INTERCESSION</span>
                        </td>
                    </tr>
                    <tr>
                        <td class="bordertd">
                            <span class="spanletter">J</span>
                        </td>
                    </tr>
                    <tr>
                        <td class="bordertd">
                            <span class="spanletter">M</span>
                        </td>
                    </tr>
                </table>
            </v-col>
        </v-row>

        <v-row dense>
            <v-col lg="3"></v-col>
            <v-col lg="6">
                <table style="width: 100%;">
                    <tr style="text-align: center;">
                        <td class="bordertd2">
                            <span class="spanvision">VISION</span>
                        </td>
                    </tr>
                    <tr style="text-align: center;">
                        <td>
                            <span class="spanpray">PRAY PRAY PRAY PRAY PRAY PRAY PRAY</span>
                        </td>
                    </tr>
                    <tr style="text-align: center;">
                        <td>
                            <span class="spanpray">PRAY PRAY PRAY PRAY PRAY PRAY PRAY PRAY</span>
                        </td>
                    </tr>
                </table>
            </v-col>
            <v-col lg="3"></v-col>
        </v-row>

        <v-row dense class="mt-6">
            <v-col lg="9">
                <table style="width: 100%;">
                    <tr>
                        <td class="events">
                            <v-row>
                                <v-col lg="3">
                                    <span>Previous Events</span>
                                </v-col>
                                <v-col lg="7" class="mt-6">
                                    <span ><v-divider color="white"></v-divider></span>
                                </v-col>
                                <v-col lg="2"></v-col>
                            </v-row>
                        </td>
                    </tr>
                    <tr>
                        <td>
                            <template>
                                <v-sheet
                                    max-width="800"
                                    style="background-color: transparent;"
                                >
                                    <v-slide-group
                                    show-arrows
                                    prev-icon="mdi-arrow-left-drop-circle"
                                    next-icon="mdi-arrow-right-drop-circle"
                                    >
                                    <v-slide-item
                                        v-for="(source, index) in videoSources" :key="index"
                                        v-slot="{ active, toggle }"
                                    >
                                        <v-card
                                        :color="active ? 'primary' : 'grey lighten-1'"
                                        class="ma-4"
                                        height="200"
                                        width="200"
                                        @click="toggle"
                                        >
                                        <video controls height="200"
                                        width="200">
                                            <source :src="'/videos/' + source" type="video/mp4">
                                        </video>
                                        </v-card>
                                    </v-slide-item>
                                    </v-slide-group>
                                </v-sheet>
                                </template>
                        </td>
                    </tr>
                </table>
            </v-col>
            <v-col lg="3" style="margin-top: 210px;">
                <v-row dense>
                    <v-col lg="12">
                        <table cellspacing="0" cellpadding="0">
                            <tr>
                                <td class="btn">
                                    <v-btn block color="#0000CD">
                                        <span class="white--text">Join Now!</span>
                                    </v-btn>
                                </td>
                                <td class="btn">
                                    <v-btn block color="#0000CD">
                                        <span class="white--text">Explore</span>
                                    </v-btn>
                                </td>
                                <td class="btn">
                                    <v-btn block color="#0000CD">
                                        <span class="white--text">Donate</span>
                                    </v-btn>
                                </td>
                            </tr>
                        </table>
                        
                    </v-col>
                </v-row>
            </v-col>
        </v-row>
    </div>
    
</template>

<script>
export default {
    data(){
        return {
            videoSources: [
                'rain.mp4',
                'rick1.mp4',
                'rick2.mp4',
                'rick3.mp4',
                'rick4.mp4',
            ]
        }
    }
}
</script>

<style scoped>
.bordertd {
    border-collapse: collapse;
    border-right: 4px solid white;
    padding: 0;
    margin: 0;
    display: flex;
}

.bordertd2 {
    border-collapse: collapse;
    border-bottom: 2px solid white;
}

.spanletter {
    color: white; 
    font-size: 58px;
}

.spanintercession {
    color: white; 
    font-size: 30px;
    font-family: Georgia, 'Times New Roman', Times, serif;
}

.spanvision {
    color: white; 
    font-size: 35px; 
    text-align: center;
    font-family: Georgia, 'Times New Roman', Times, serif;
}

.spanpray {
    color: white; 
    font-size: 25px; 
    text-align: center;
    font-family: Georgia, 'Times New Roman', Times, serif;
}

.events {
    color:white;
    font-size: 25px;
}

.btn {
    width: 30px;
    border-collapse: collapse;
    border: 1px solid white;
}


</style>