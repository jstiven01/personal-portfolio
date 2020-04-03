<template>
  <div class="home">
    <v-img
      dark
      max-height="500px"
      class="white--text align-end"
      src="https://images.unsplash.com/photo-1488590528505-98d2b5aba04b?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=500&q=60"
    >
      <v-container fill-height>
        <v-row>
          <v-col
            cols="12"
            justify="end"
            align-self="stretch"
            class="white--text"
          >
            <div :class="getFontSize">
              <strong> Let's build some Apps. </strong>
            </div>
          </v-col>
        </v-row>
      </v-container>
    </v-img>
    <v-container class="mt-5">
      <v-row>
        <v-col cols="12">
          <div
            id="about"
            class="display-1"
          >
            About me
          </div>
        </v-col>
        <v-col cols="12">
          <div class="body-1 px-4">
            {{ aboutText }}
          </div>
        </v-col>
      </v-row>
      <v-row>
        <v-col cols="12">
          <div
            id="portfolio"
            class="display-1"
          >
            My Work
          </div>
        </v-col>
        <v-col>
          <Portfolio />
        </v-col>
      </v-row>              
      <v-row>
        <v-col cols="12">
          <div
            id="contact"
            class="display-1"
          >
            Contact
          </div>
        </v-col>
        <v-col cols="12">
          <Contact />
        </v-col>
      </v-row>
    </v-container>
  </div>
</template>

<script>
// @ is an alias to /src
import Portfolio from '@/components/Portfolio'
import Contact from '@/components/Contact'

export default {
  name: 'Home',
  components: {
    Portfolio,
    Contact


  },
  data(){
    return{
      aboutText: "I have been a software developer for more than 15 years at different systems like financial, ERP, open-source systems, etc. Currently, I am passionate about web development and Machine Learning. A person with teamwork abilities, strengths in objective decision making, willingness for learning and knowledge, skilled at development and testing software, planning, management and implementation of projects.",

    };
  },
  computed:{
        getFontSize(){
              return this.$vuetify.breakpoint.xs ? 'title': 'headline'
          },
  }
}
</script>
