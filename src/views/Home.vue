<template>
  <div class="home">
    <v-img
      dark
      max-height="500px"
      src="https://images.unsplash.com/photo-1488590528505-98d2b5aba04b?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=500&q=60"
    >
      >

      <v-container fill-height>
        <v-row>
          <v-col
            cols="12"
            justify="end"
            align-self="stretch"
            class="white--text"
          >
            <div class="title black">
              <strong> Let's buid some Apps </strong>
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
          <div class="body-1">
            {{ aboutText }}
          </div>
          <div class="body-1">
            Working Microverse
          </div>
        </v-col>
      </v-row>
      <div
        class="height-long"
        style="height: 600px;"
      />
      <v-row>
        <v-col>
          <div
            id="portfolio"
            class="display"
          >
            My Work
          </div>
        </v-col>
        <v-col>
          <Portfolio />
          <!-- <template v-for="(app, i) in apps">

          </template>-->
        </v-col>
      </v-row>
      <div
        class="height-long"
        style="height: 600px;"
      />               
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
      aboutText: "I am a software developer for more than 15 years at different systems like financial, ERP, open source systems etc. Currently I am passionated about Web development and Machine Learning. A person with team work abilities, strengths in objective decision making, willingness for learning and knowledge, skilled at development and testing software, planning, management and implementation of projects.",
      apps: [
        {
          name: "Food Vision",
          price: "FREE",
          logo: "food-vision-logo.png",
          platforms: [
            {
              name: "apple",
              icon: "mdi-apple",
              link: "https://apps.apple.com/us/app/food-vision/id1437083324"
            }
          ],
          description:
            "One day my friend and I were eating at a restaurant and she suddenly asked me what an item looks like. I looked up at her an told her I didnt know. Then she told me why dont you make an app where you can see the pictures of food thats on the menu? Then I made Food Vision. :)",
          technologies: [
            {
              name: "Swift",
              icon: "mdi-language-swift",
              link: ""
            },
            {
              name: "XCode",
              icon: "mdi-apple-ios",
              link: ""
            },
            {
              name: "Firebase",
              icon: "mdi-firebase",
              link: ""
            }
          ],
          code: {
            name: "github",
            icon: "mdi-github-circle",
            link: ""
          }
        },
        {
          name: "Finance App",
          price: "COMING SOON",
          logo: "finance-logo.png",
          platforms: [
            {
              name: "apple",
              icon: "mdi-apple",
              link: ""
            },
            {
              name: "android",
              icon: "mdi-android",
              link: ""
            }
          ],
          description:
            "My sister always kept asking me about my money situation and how I was doing there, so I decided that I would make an app that we could use to track our finances. Using Plaid I was able to get access to my bank account and hers and connect the 2 using firebase Functions and Auth to secure the app. ",
          technologies: [
            {
              name: "VueJS",
              icon: "mdi-vuejs",
              link: ""
            },
            {
              name: "Vuetify",
              icon: "mdi-vuetify",
              link: ""
            },
            {
              name: "Cordova",
              icon: "mdi-cordova",
              link: ""
            },
            {
              name: "Firebase",
              icon: "mdi-firebase",
              link: ""
            },
            {
              name: "Node",
              icon: "mdi-nodejs",
              link: ""
            }
          ],
          code: {
            name: "github",
            icon: "mdi-github-circle",
            link: "https://github.com/uzirthapa/finance-app"
          }
        },
        {
          name: "Baguette",
          price: "COMING SOON",
          logo: "baguette-logo.png",
          platforms: [
            {
              name: "apple",
              icon: "mdi-apple",
              link: ""
            },
            {
              name: "android",
              icon: "mdi-android",
              link: ""
            }
          ],
          description:
            "Similar to 'Bag it'. I wanted to make a swippable market place where people could swipe on goods from a store. Also it got rid of all the extra distractions and you are able to focus on just one item at a time. Still need to build the recommender system. But I am working on it! :)",
          technologies: [
            {
              name: "VueJS",
              icon: "mdi-vuejs",
              link: ""
            },
            {
              name: "Vuetify",
              icon: "mdi-vuetify",
              link: ""
            },
            {
              name: "Cordova",
              icon: "mdi-cordova",
              link: ""
            },
            {
              name: "Firebase",
              icon: "mdi-firebase",
              link: ""
            }
          ],
          code: {
            name: "github",
            icon: "mdi-github-circle",
            link: ""
          }
        },
        {
          name: "Facebook UI",
          price: "OPEN SOURCE",
          logo: "facebook-logo.png",
          platforms: [
            {
              name: "web",
              icon: "mdi-web",
              link: "https://uzirthapa.github.io/facebook-ui/dist/"
            }
          ],
          description:
            "One Day build - I saw this guy on youtube building apps in 1 day and I wanted to see if I could make a better version of the Facebook UI. I didn't design it but I found this design on dribbble and just thought I would make the designers UI come to life.",
          technologies: [
            {
              name: "VueJS",
              icon: "mdi-vuejs",
              link: ""
            },
            {
              name: "Vuetify",
              icon: "mdi-vuetify",
              link: ""
            }
          ],
          code: {
            name: "github",
            icon: "mdi-github-circle",
            link: "https://github.com/uzirthapa/facebook-ui"
          }
        },
        {
          name: "Firebird Fitness",
          price: "LIVE",
          logo: "firebird-logo.png",
          platforms: [
            {
              name: "web",
              icon: "mdi-web",
              link: "https://firebirdfitness.xyz/"
            }
          ],
          description:
            "I needed a place to put my workouts that we do at work, So I made a place where I could store them and also if I forgot a certian exercise I could easily search it and watch a video on how to do it.",
          technologies: [
            {
              name: "VueJS",
              icon: "mdi-vuejs",
              link: "https://vuejs.org/"
            },
            {
              name: "Vuetify",
              icon: "mdi-vuetify",
              link: "https://vuetifyjs.com/"
            },
            {
              name: "Firebase",
              icon: "mdi-firebase",
              link: "https://firebase.google.com/"
            }
          ],
          code: {
            name: "github",
            icon: "mdi-github-circle",
            link: "https://github.com/uzirthapa/Firebird-Fitness"
          }
        },
        {
          name: "Ecommerce App",
          price: "$50.00",
          logo: "logo.png",
          platforms: [
            {
              name: "web",
              icon: "mdi-web",
              link: "https://ecommerce-skeleton.firebaseapp.com/"
            }
          ],
          description:
            "We Wanted to help people who want to create an ecommerce store with VueJS and Vuetify have a template that had authentication and payments integrated right from the get go. So now you can hit the ground running! In Collaboration with Aatish Balla.",
          technologies: [
            {
              name: "VueJS",
              icon: "mdi-vuejs",
              link: "https://vuejs.org/"
            },
            {
              name: "Vuetify",
              icon: "mdi-vuetify",
              link: "https://vuetifyjs.com/"
            },
            {
              name: "Firebase",
              icon: "mdi-firebase",
              link: "https://firebase.google.com/"
            },
            {
              name: "Stripe",
              icon: "mdi-credit-card-outline",
              link: ""
            }
          ],
          code: {
            name: "github",
            icon: "mdi-github-circle",
            link: ""
          }
        },
        {
          name: "Sacred Summits",
          price: "LIVE",
          logo: "ss-logo-high-res.png",
          platforms: [
            {
              name: "web",
              icon: "mdi-web",
              link: "https://sacred-summits-web.firebaseapp.com/"
            }
          ],
          description:
            "Sacred Summits was looking for a redesign of their website and they asked me to come up with a sample. This is what I came up with.",
          technologies: [
            {
              name: "VueJS",
              icon: "mdi-vuejs",
              link: "https://vuejs.org/"
            },
            {
              name: "Vuetify",
              icon: "mdi-vuetify",
              link: "https://vuetifyjs.com/"
            },
            {
              name: "Firebase",
              icon: "mdi-firebase",
              link: "https://firebase.google.com/"
            }
          ],
          code: {
            name: "github",
            icon: "mdi-github-circle",
            link: ""
          }
        }
      ],
    };
  }
}
</script>
