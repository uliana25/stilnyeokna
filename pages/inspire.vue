<template>
  <v-container fluid>
    <v-layout row justify-center>
      <v-flex>
         <img src="slide1.jpg" alt="alutech">
      </v-flex>  
    </v-layout>
    <v-layout>
        <v-flex xs4>
          <v-card>
            <v-card-media
              class="white--text"
              height="300px"
              src="window.png"
            >
            </v-card-media>
            <v-card-title color="grey"> 
              <div>
                <span class="grey--text">МПО</span><br>
                <span>На украинском рынке металлопластиковые окна появились 
                  не так давно. Но это вовсе не означает, что данная продукция «молодая», 
                  так как на мировом рынке она представлена и пользуется большим спросом у 
                  потребителей уже очень длительное время.</span><br>
              </div>
            </v-card-title>
            <v-card-actions>
                <router-link :to="{ name: 'index' }"><v-btn flat color="orange">Подробнее</v-btn>
                </router-link>  
            </v-card-actions>
          </v-card>
        </v-flex>
        <v-flex xs4>
            <v-card>
              <v-card-media
                class="white--text"
                height="300px"
                src="rol.jpg"
              >
              </v-card-media>
              <v-card-title color="grey"> 
                <div>
                  <span class="grey--text">Роллеты</span><br>
                  <span>На украинском рынке металлопластиковые окна появились 
                    не так давно. Но это вовсе не означает, что данная продукция «молодая», 
                    так как на мировом рынке она представлена и пользуется большим спросом у 
                    потребителей уже очень длительное время.</span><br>
                </div>
              </v-card-title>
              <v-card-actions>
                  <router-link :to="{ name: 'index' }"><v-btn flat color="orange">Подробнее</v-btn>
                  </router-link>  
              </v-card-actions>
            </v-card>
          </v-flex>
          <v-flex xs4>
              <v-card>
                <v-card-media
                  class="white--text"
                  height="300px"
                  src="maf.jpg"
                >
                </v-card-media>
                <v-card-title color="grey"> 
                  <div>
                    <span class="grey--text">МАФЫ</span><br>
                    <span>На украинском рынке металлопластиковые окна появились 
                      не так давно. Но это вовсе не означает, что данная продукция «молодая», 
                      так как на мировом рынке она представлена и пользуется большим спросом у 
                      потребителей уже очень длительное время.</span><br>
                  </div>
                </v-card-title>
                <v-card-actions>
                    <router-link :to="{ name: 'index' }"><v-btn flat color="orange">Подробнее</v-btn>
                    </router-link>  
                </v-card-actions>
              </v-card>
            </v-flex>
      </v-layout>
     </v-container>  		 
  
</template>
<style scoped>  
   a:link { text-decoration: none;
   color: white
    }
    a:visited { text-decoration: none;
      color: white }
    a:active { text-decoration: none;
      color: white }
    a:hover { 
     text-decoration: none; 
     color: rgb(216, 208, 208); 
   } 
   .pos {
     position: absolute;
     bottom: 0px;
   }
</style>
<script>
  export default {
    data () {
      return {
        items: [
          {
            src: 'slide1.jpg'
          },
          {
            src: 'slide2.jpg'
          },
          {
            src: 'slide3.jpg'
          }
        ]
      }
    }
  }
</script> 
