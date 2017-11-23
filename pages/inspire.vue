<template>
  <v-container fluid>
    <v-layout row>
      <v-flex xs4>
        <v-card>
          <v-card-media
          class="grey--text"
            height="270px"
            src="window.png"
            
          >
          </v-card-media>
          <v-card-text>
            <div>
                <router-link :to="{ name: 'index' }"> <h4 class="text-xs-center">МПО</h4></router-link>
            </div>
          </v-card-text>
        </v-card>
      </v-flex>
      <v-flex xs4>
          <v-card>
            <v-card-media
            class="grey--text"
              height="270px"
              src="maf.jpg"
            >
            </v-card-media>
            <v-card-text>
              <div>
                  <router-link :to="{ name: 'index' }"> <h4 class="text-xs-center">МАФЫ</h4></router-link>
              </div>
            </v-card-text>
          </v-card>
        </v-flex>
        <v-flex xs4>
            <v-card>
              <v-card-media
              class="grey--text"
                height="270px"
                src="rollet.jpg"
              >
              </v-card-media>
              <v-card-text>
                <div>
                    <router-link :to="{ name: 'index' }"> <h4 class="text-xs-center">Роллеты</h4></router-link>
                </div>
              </v-card-text>
            </v-card>
          </v-flex>
    </v-layout>
  </v-container>
</template>  
