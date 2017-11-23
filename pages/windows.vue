<template>
  <v-container fluid>
    <v-layout row>
      <v-flex 12xs>
        <v-tabs fixed centered>
          <v-toolbar extended color="grey darken-1" dark>
            <v-toolbar-title slot="extension" class="display-2">Окна</v-toolbar-title>
          </v-toolbar>
          <v-tabs-bar color="grey darken-1" dark>
            <v-tabs-item>
            <router-link to="/windows/renau">Renau</router-link>
            </v-tabs-item>
            <v-tabs-item>
            <router-link to="/windows/kbe">KBE</router-link>
            </v-tabs-item>
            <v-tabs-item>
            <router-link to="/windows/openteck">OpenTeck</router-link>
            </v-tabs-item>
          </v-tabs-bar>
        </v-tabs>
      </v-flex>
    </v-layout>
    <v-layout>
      <v-flex 12xs>
        <nuxt-child></nuxt-child>
      </v-flex>
    </v-layout>
  </v-container>
</template>
<style>
  a:link { 
    text-decoration: none;
    color: white; 
  } 
  a:visited { 
     text-decoration: none; 
     color: white; 
  } 
   a:active { text-decoration: none;
    color: white; 
     }
   a:hover {
    text-decoration: underline; 
    color: white; 
   } 
</style>
<script>
  export default {
    data () {
      return {
        items: ['Renau', 'KBE', 'OpenTeck']
      }
    }
  }
</script>