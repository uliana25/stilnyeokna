<template>
  <v-layout column justify-center align-center>
    <v-flex xs12 sm8 md6>
      <div class="text-xs-center">
        <img src="/window.png" alt="StilnyeOkna.com" height="250px" class="mb-5" />
      </div>
      <v-card>
        <v-card-title class="headline">Hello, Uli! Now i'm in SPA mode.</v-card-title>
        <v-card-text>
          <div class="text-xs-right">
            <p>На странице «Inspire» можно играться и экспериментировать.</p>
            <em><small>&mdash; NZXTUA</small></em>
          </div>
        </v-card-text>
        <v-card-actions>
          <v-spacer></v-spacer>
          <v-btn color="primary" flat nuxt :to="{ name: 'inspire' }">Continue</v-btn>
        </v-card-actions>
      </v-card>
    </v-flex>
  </v-layout>
</template>

<script>
  export default {
  }
</script>  