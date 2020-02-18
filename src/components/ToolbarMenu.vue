<template>
  <v-toolbar>
    <v-toolbar-title>Toolbar Mobile Menu</v-toolbar-title>
    <v-spacer />
    <v-toolbar-items class="hidden-sm-and-down">
      <v-btn
        v-for="item in menu"
        :key="item.icon"
        :to="item.link"
        text
      >
        {{ item.title }}
      </v-btn>
    </v-toolbar-items>
    <template v-slot:activator="{ on }">
      <v-menu class="hidden-md-and-up">
        <v-app-bar-nav-icon v-on="on" />

        <v-list>
          <v-list-tile
            v-for="item in menu"
            :key="item.icon"
          >
            <v-list-tile-content>
              <v-list-tile-title>{{ item.title }}</v-list-tile-title>
            </v-list-tile-content>
          </v-list-tile>   
        </v-list>
      </v-menu>
    </template>
  </v-toolbar>
</template>

<script>
export default {
    data () {
    return {
      menu: [
        { icon: 'home', title: 'Link A' },
        { icon: 'info', title: 'Link B' },
        { icon: 'warning', title: 'Link C' }
      ]
    }
  },
  
  methods: {
    menuItems () {
      return this.menu
    }
  }
}
</script>