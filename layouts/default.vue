<template>
  <v-app light>

    <v-toolbar fixed app :clipped-left="clipped" :extended="currentRoute">
      <v-toolbar-title class="white--text" v-for="item in items"></v-toolbar-title>
      <v-toolbar-title class="grey--text" slot="extension" v-for="item in subItems">{{item.title}}</v-toolbar-title>
      
      <router-link :to="{ name: 'index' }">
        <img
          src="/stilnyeokna-logo.jpg"
          height="55px"
          alt="StilnyeOkna.com"
        >
      </router-link>

      <v-spacer></v-spacer>

      <v-toolbar-items
        class="hidden-sm-and-down"
        v-for="item in items"
        :key="item.title"
      >
        <v-btn flat router exact :to="item.to">
          <v-icon v-html="item.icon"></v-icon>
          {{ item.title }}
        </v-btn>
      </v-toolbar-items>

      <v-toolbar-side-icon class="hidden-md-and-up" @click="drawer = !drawer"></v-toolbar-side-icon>
    </v-toolbar>

    <v-content>
      <v-container>
        <nuxt />
      </v-container>
    </v-content>

    <v-navigation-drawer
      disable-resize-watcher
      disable-route-watcher
      :clipped="clipped"
      v-model="drawer"
      right
      fixed
      app
    >
      <v-list>
        <v-list-tile 
          router
          exact
          :to="item.to"
          :key="i"
          v-for="(item, i) in items"
        >
          <v-list-tile-action>
            <v-icon v-html="item.icon"></v-icon>
          </v-list-tile-action>
          <v-list-tile-content>
            <v-list-tile-title v-text="item.title"></v-list-tile-title>
          </v-list-tile-content>
        </v-list-tile>
      </v-list>
    </v-navigation-drawer>

    <v-footer app>
      <span>&copy; 2017</span>
    </v-footer>
  </v-app>
</template>

<script>
  import items from '@/assets/navigation'

  export default {
    data () {
      return {
        active: false,
        title: 'StilnyeOkna',
        items,
        drawer: false,
        clipped: false
      }
    },

    computed: {
      subItems () {
        const currentRoute = this.$route.path || ''
        const item = this.items.find(el => el.to === currentRoute)
        return item.sub
      }
    }
  }
</script>
