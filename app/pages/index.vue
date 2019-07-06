<template>
  <div>
    <v-container grid-list-md text-xs-center>
      <v-layout row wrap>
        <v-flex xs12>
          <v-parallax dark :src="require('@/assets/facebook.png')">
            <v-layout align-center column justify-center>
              <!-- <h1 class="display-2 font-weight-thin mb-3">fplist</h1> -->
              <h1 style="margin-top:420px;">
                駆け出したいエンジニアに再び光を
              </h1>
            </v-layout>
          </v-parallax>
        </v-flex>
        <v-flex xs4>
          <v-card>
            <v-card-text class="px-0"
              ><span class="group pa-2">
                <v-icon large style="font-size:60px">create</v-icon>
              </span></v-card-text
            >
            <div style="font-size:16px;padding-bottom:12px;">
              ポートフォリオを作る際に迷わなくする
            </div>
          </v-card>
        </v-flex>
        <v-flex xs4>
          <v-card>
            <v-card-text class="px-0"
              ><span class="group pa-2">
                <v-icon large style="font-size:60px">folder_open</v-icon>
              </span></v-card-text
            >
            <div style="font-size:16px;padding-bottom:12px;">
              技術ナレッジを共有するプラットフォーム
            </div>
          </v-card>
        </v-flex>
        <v-flex xs4>
          <v-card>
            <v-card-text class="px-0"
              ><span class="group pa-2">
                <v-icon large style="font-size:60px">how_to_reg</v-icon>
              </span></v-card-text
            >
            <div style="font-size:16px;padding-bottom:12px;">
              エンジニアとの繋がりを増やす
            </div>
          </v-card>
        </v-flex>
        <v-flex v-for="i in 8" :key="`3${i}`" xs4 text-xs-left>
          <v-card>
            <v-card>
              <v-img
                v-if="i % 2 === 0"
                src="https://cdn.vuetifyjs.com/images/cards/desert.jpg"
                aspect-ratio="1.50"
              ></v-img>
              <v-img
                v-else
                :src="require('@/assets/portfolio.png')"
                aspect-ratio="1.50"
              ></v-img>
              <v-card-title primary-title>
                <div>
                  <h3 class="headline mb-0">
                    <nuxt-link :to="{ name: 'detail-id', params: { id: i } }"
                      >なおとのportfolio</nuxt-link
                    >
                  </h3>
                  <div class="mb-3">
                    ポートフォリオを集約するサイトです。技術はNuxt.jsやGoを使用しています。２人でチーム開発をしています。プルリク大歓迎です！！
                  </div>
                  <div>
                    <v-chip outline color="secondary">Vue</v-chip
                    ><v-chip outline color="secondary">TypeScript</v-chip
                    ><v-chip outline color="secondary">Go</v-chip>
                    <v-chip outline color="secondary">AWS</v-chip>
                  </div>
                </div>
              </v-card-title>
              <v-list-tile class="grow" style="padding-bottom:16px;">
                <v-list-tile-avatar color="grey darken-3">
                  <v-img
                    class="elevation-6"
                    src="https://avatars0.githubusercontent.com/nsuzuki7713"
                  ></v-img>
                </v-list-tile-avatar>

                <v-list-tile-content>
                  <v-list-tile-title
                    >なおと(<a
                      href="https://twitter.com/naoto_7713?lang=ja"
                      target="_blank"
                      >@naoto_7713</a
                    >)</v-list-tile-title
                  >
                  <v-list-tile-sub-title
                    >更新日:2019/07/04</v-list-tile-sub-title
                  >
                </v-list-tile-content>
                <v-card-actions>
                  <v-btn flat icon color="pink">
                    <v-icon>favorite</v-icon>
                  </v-btn>
                  <span>10</span>
                </v-card-actions>
              </v-list-tile>
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
