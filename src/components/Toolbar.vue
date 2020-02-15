<template>
    <v-app-bar flat absolute color="red" dark height="120px">
        <v-container>
            <v-layout justify-center="">
                <v-flex>
                    <div class="display-1 font-weight-bold">
                    Johan Stiven Tinjaca
                    </div>
                    <v-subheader>Full Stack Developer</v-subheader>                    
                </v-flex>

            <v-spacer></v-spacer>
            <v-toolbar-items>
                <v-btn color="success" @click="$vuetify.goTo('#about', options)">About</v-btn>
                <v-btn color="success" @click="$vuetify.goTo('#portfolio', options)">My work</v-btn>
                <v-btn color="success" @click="$vuetify.goTo('#contact', options)">Contact</v-btn>
            </v-toolbar-items>
        </v-layout>
            
        </v-container>

    </v-app-bar>
</template>

<script>
export default {
    name: "Toolbar",
    data(){
        return {
            options: {
            duration: 300,
            offset: 0,
            easing: "easeInOutCubic"
       }
        }
    }
}
</script>