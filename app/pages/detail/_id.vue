<template>
  <div>
    <v-container grid-list-md>
      <v-layout row wrap>
        <v-flex xs6>
          <v-card dark color="secondary">
            <v-carousel>
              <v-carousel-item
                v-for="(item, i) in items"
                :key="i"
                :src="item.src"
              ></v-carousel-item>
            </v-carousel>
          </v-card>
        </v-flex>
        <v-flex xs6>
          <v-card style="padding:16px;">
            <v-card-text class="px-0">
              <div v-if="editFlag">
                <v-text-field label="ポートフォリオ名"></v-text-field>
                <v-textarea label="概要"></v-textarea>
              </div>
              <div v-else>
                <h1>なおとのportfolio</h1>
                <div>
                  ポートフォリオを集約するサイトです。技術はNuxt.jsやGoを使用しています。２人でチーム開発をしています。プルリク大歓迎です！！
                </div>
              </div>
              <v-list-tile class="grow" style="padding-top:20px;">
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
            </v-card-text>
          </v-card>
        </v-flex>
        <v-flex xs12>
          <v-card style="padding:16px;">
            <h1>使用技術・ツール</h1>
            <div v-if="editFlag">
              <v-text-field label="スキル"></v-text-field>
            </div>
            <div v-else>
              <v-card-text class="px-0"
                ><v-chip outline color="secondary">Vue</v-chip
                ><v-chip outline color="secondary">TypeScript</v-chip
                ><v-chip outline color="secondary">Go</v-chip>
                <v-chip outline color="secondary">AWS</v-chip>
                <v-chip outline color="secondary">MySql</v-chip>
                <v-chip outline color="secondary">Docker</v-chip>
                <v-chip outline color="secondary">Nuxt.js</v-chip>
                <v-chip outline color="secondary">Vuetify</v-chip>
                <v-chip outline color="secondary">PlantUML</v-chip>
              </v-card-text>
            </div>
          </v-card>
        </v-flex>
        <v-flex xs12>
          <v-card style="padding:16px;">
            <h1>詳細</h1>
            <div v-if="editFlag">
              <v-textarea label="詳細"></v-textarea>
            </div>
            <div v-else>
              <v-card-text class="px-0"
                >ポートフォリオを集約するサイトです。技術はNuxt.jsやGoを使用しています。２人でチーム開発をしています。プルリク大歓迎です！！ポートフォリオを集約するサイトです。技術はNuxt.jsやGoを使用しています。<br />２人でチーム開発をしています。プルリク大歓迎です！！ポートフォリオを集約するサイトです。技術はNuxt.jsやGoを使用しています。<br />２人でチーム開発をしています。プルリク大歓迎です！！ポートフォリオを集約するサイトです。技術はNuxt.jsやGoを使用しています。２人でチーム開発をしています。プルリク大歓迎です！！</v-card-text
              >
            </div>
          </v-card>
        </v-flex>
        <v-flex xs6>
          <v-card style="padding:16px;">
            <h1>成果物リンク</h1>
            <div v-if="editFlag">
              <v-text-field label="ポートフォリオ"></v-text-field>
              <v-text-field label="Github"></v-text-field>
              <v-text-field label="Qiita"></v-text-field>
            </div>
            <div v-else>
              <v-card-text class="px-0">
                <h2>
                  <a
                    href="https://github.com/haruto830/pflist-backend"
                    target="_blank"
                    >ポートフォリオ</a
                  >
                </h2>
                <h2>
                  <a
                    href="https://github.com/haruto830/pflist-backend"
                    target="_blank"
                    >Github</a
                  >
                </h2>
                <h2>
                  <a
                    href="https://github.com/haruto830/pflist-backend"
                    target="_blank"
                    >Qiita</a
                  >
                </h2>
              </v-card-text>
            </div>
          </v-card>
        </v-flex>
        <v-flex xs6>
          <v-card style="padding:16px;">
            <h1>ステータス</h1>
            <div v-if="editFlag">
              <v-text-field label="期間"></v-text-field>
              <v-text-field label="状態"></v-text-field>
            </div>
            <div v-else>
              <v-card-text class="px-0">
                期間: 4ヶ月 <br />状態: 開発中 <br />追加日: 2019/07/06
                <br />更新日: 2019/07/06
              </v-card-text>
            </div>
          </v-card>
        </v-flex>
      </v-layout>
      <div style="text-align: center;">
        <v-btn color="success">登録</v-btn>
        <v-btn color="error">削除</v-btn>
        <v-btn color="warning">更新</v-btn>
        <v-btn color="warning" @click="editFlag = !editFlag">編集</v-btn>
      </div>
    </v-container>
  </div>
</template>
<script>
import PortfolioImage from '~/assets/portfolio.png'

export default {
  asyncData({ params }) {
    return {
      id: params.id,
      items: [
        {
          src: PortfolioImage
        },
        {
          src: 'https://cdn.vuetifyjs.com/images/carousel/squirrel.jpg'
        },
        {
          src: 'https://cdn.vuetifyjs.com/images/carousel/sky.jpg'
        }
      ],
      editFlag: false
    }
  }
}
</script>
