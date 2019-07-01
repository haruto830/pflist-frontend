<template>
  <div>
    <v-container grid-list-md text-xs-center>
      <v-layout row wrap>
        <v-flex xs12>
          <v-parallax dark :src="require('@/assets/facebook.png')">
            <v-layout align-center column justify-center>
              <!-- <h1 class="display-2 font-weight-thin mb-3">fplist</h1> -->
              <h1 class="subheading" style="margin-top:390px;">
                駆け出したいエンジニアに再び光を
              </h1>
            </v-layout>
          </v-parallax>
        </v-flex>
        <v-flex xs4>
          <v-card dark color="primary">
            <v-card-text class="px-0"
              ><span class="group pa-2">
                <v-icon large>folder_open</v-icon>
              </span></v-card-text
            >
            <div>pflistの簡単な紹介文を書く？？？？？</div>
          </v-card>
        </v-flex>
        <v-flex xs4>
          <v-card dark color="primary">
            <v-card-text class="px-0"
              ><span class="group pa-2">
                <v-icon large>folder_open</v-icon>
              </span></v-card-text
            >
            <div>pflistの簡単な紹介文を書く？？？？？</div>
          </v-card>
        </v-flex>
        <v-flex xs4>
          <v-card dark color="primary">
            <v-card-text class="px-0"
              ><span class="group pa-2">
                <v-icon large>folder_open</v-icon>
              </span></v-card-text
            >
            <div>pflistの簡単な紹介文を書く？？？？？</div>
          </v-card>
        </v-flex>
        <v-flex v-for="i in 8" :key="`3${i}`" xs3>
          <v-card dark color="secondary">
            <v-card>
              <v-img
                src="https://cdn.vuetifyjs.com/images/cards/desert.jpg"
                aspect-ratio="1.50"
              ></v-img>
              <v-card-title primary-title>
                <div>
                  <h3 class="headline mb-0">なおとのportfolio</h3>
                  <div>
                    こんにちわポートフォリオです。とてもむずかしかったです。
                  </div>
                  <div>
                    <v-chip outline color="secondary">Vue</v-chip
                    ><v-chip outline color="secondary">TypeScript</v-chip
                    ><v-chip outline color="secondary">Go</v-chip>
                  </div>
                </div>
              </v-card-title>
              <v-card-actions>
                <v-btn flat icon color="pink">
                  <v-icon>favorite</v-icon>
                </v-btn>
                <span>10</span>
              </v-card-actions>
            </v-card>
          </v-card>
        </v-flex>
        <v-flex xs12>
          <v-pagination v-model="page" :length="6"></v-pagination>
        </v-flex>
      </v-layout>
    </v-container>
  </div>
</template>
<script>
export default {
  data() {
    return {
      page: 1,
      items: [
        {
          src: 'https://cdn.vuetifyjs.com/images/carousel/squirrel.jpg'
        },
        {
          src: 'https://cdn.vuetifyjs.com/images/carousel/sky.jpg'
        },
        {
          src: 'https://cdn.vuetifyjs.com/images/carousel/bird.jpg'
        },
        {
          src: 'https://cdn.vuetifyjs.com/images/carousel/planet.jpg'
        }
      ]
    }
  }
}
</script>
