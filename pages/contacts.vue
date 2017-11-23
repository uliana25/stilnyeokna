<template>
  <v-layout>
    <v-flex justify-center>

      <v-card>
        <v-card-media src="/window.png" alt="StilnyeOkna.com" height="100%">
          <v-layout justify-space-around wrap>
            <v-flex xs12 sm4>
              <v-card-title primary-title text-xs-start>
                <div>
                  <div class="display-1 mb-3">
                    {{ company.name }}
                  </div>
                  <div
                    class="subheading"
                    v-html="company.slogan"
                  >
                  </div>
                </div>
              </v-card-title>
           </v-flex>    
           <v-flex xs12 sm4>
              <v-card-text class="px-5 bordered-left">
                <div class="mb-3">
                  <span class="title">Почта:</span>
                  <div class="mx-3">{{ company.email }}</div>
                </div>
    
                <div class="mb-3">
                  <span class="title">Телефоны:</span>
                  <div
                    v-for="item in company.phones"
                    :key="item.number"
                    class="mx-3"
                  >
                    <span>
                      {{item.number}}
                      <sup
                        :class="`${item.color}--text`">
                        {{ item.title }}
                      </sup>
                    </span>
                  </div>
                </div>
    
                <div>
                  <span class="title">Адрес:</span>
                  <div class="mx-3"
                    v-html="company.address"
                  >
                  </div>
                </div>
              </v-card-text>
           </v-flex>
          </v-layout>
        </v-card-media>
      </v-card>

    </v-flex>
  </v-layout>
</template>


<script>
  export default {
    data () {
      return {
        client: {
          name: null,
          email: null,
          phone: null,
          message: null
        },
        company: {
          name: 'Стильные Окна',
          slogan: 'Роллеты, ворота и автоматика "Алютех"<br/>Металлопластиковые окна<br/>Металлоконструкции',
          phones: [
            { title: 'Городской', number: '(0462) 611-505', color: 'blue-grey' },
            { title: 'Vodafone', number: '(066) 347-71-21', color: 'red' },
            { title: 'Life:)', number: '(073) 488-15-51', color: 'deep-orange' }
          ],
          email: 'stilnyeokna@mail.ua',
          address: 'Украина, г. Чернигов,<br/>ул. Индустриальная 11в'
        }
      }
    }
  }
</script>

<style>
  .bordered-left {
    border-left: 1px dashed grey;
  }
</style>