<template>
  <v-app light>

    <v-toolbar fixed app :clipped-left="clipped">

      <router-link :to="{ name: 'index' }">
        <img
          src="/stilnyeokna-logo.jpg"
          height="50px"
          alt="stilnyeokna.com"
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
      <span>&copy; 2007-2017</span>
    </v-footer>
  </v-app>
</template>

<script>
  export default {
    data () {
      return {
        title: 'СТИЛЬНЫЕ ОКНА',
        email: 'stilnyeokna@mail.ua',
        items: [
          { icon: 'home', title: 'Главная', to: '/' },
          { icon: 'bubble_chart', title: 'Inspire', to: '/inspire' },
          { icon: 'build', title: 'Услуги', to: '/services' },
          { icon: 'perm_phone_msg', title: 'Контакты', to: '/contacts' }
        ],
        drawer: false,
        clipped: false
      }
    }
  }
</script>

<style>
  * {
    font-family: 'Exo 2', sans-serif;
  }
</style>
