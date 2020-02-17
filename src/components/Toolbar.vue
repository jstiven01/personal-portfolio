<template>
  <v-app-bar
    flat
    absolute
    color="white"
    dark
    :height="getHeight"
  >
    <v-container class="pa-0">
      <v-row no-gutters>
        <v-col
          cols="10"
          class="pa-0"
        >
          <div
            :class="getFontSize"
            class="black--text"
          >
            Johan Stiven Tinjaca
          </div>
          <div class="caption black--text pa-0">
            Full Stack Developer
          </div>                    
        </v-col>
        <v-col
          cols="2"
          class="d-flex align-end flex-column"
        >
          <v-menu offset-y>
            <template v-slot:activator="{ on }">
              <v-app-bar-nav-icon
                class="black"
                v-on="on"
              />
            </template>
            <v-list>
              <v-list-item
                color="success"
                @click="$vuetify.goTo('#about', options)"
              >
                <v-list-item-title>About me</v-list-item-title>
              </v-list-item>
              <v-list-item
                color="success"
                @click="$vuetify.goTo('#portfolio', options)"
              >
                <v-list-item-title>My Work</v-list-item-title>
              </v-list-item>
              <v-list-item
                color="success"
                @click="$vuetify.goTo('#contact', options)"
              >
                <v-list-item-title>Contact</v-list-item-title>
              </v-list-item>
            </v-list>
          </v-menu>
        </v-col>
      </v-row>
    </v-container>
  </v-app-bar>
</template>

<script>
export default {
    name: "Toolbar",
    components: {


    },
    data(){
        return {
            options: {
            duration: 300,
            offset: 0,
            easing: "easeInOutCubic"
       }
        }
    },
    computed : {
        getHeight(){
            return this.$vuetify.breakpoint.xs ? 60 : '120';
          },
          getFontSize(){
              return this.$vuetify.breakpoint.xs ? 'subheading': 'display-1'
          },
          cols () {
            const { lg, sm } = this.$vuetify.breakpoint
            return lg ? [3, 9] : sm ? [9, 3] : [10, 2]
      }
    }
}
</script>