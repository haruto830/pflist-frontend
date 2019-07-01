<template>
  <div>
    <v-container grid-list-md text-xs-center>
      <v-layout row wrap>
        <v-flex xs12>
          <v-card dark color="primary">
            <v-card-text class="px-0">〇〇のポートフォリオ</v-card-text>
          </v-card>
        </v-flex>
        <v-flex xs6>
          <v-card dark color="secondary">
            <v-card-text class="px-0"
              >アバター
              <v-avatar :tile="false" :size="300" color="grey lighten-4">
                <img
                  src="https://avatars0.githubusercontent.com/nsuzuki7713"
                  alt="avatar"
                />
              </v-avatar>
            </v-card-text>
          </v-card>
        </v-flex>
        <v-flex xs6>
          <v-card dark color="secondary">
            <v-card-text class="px-0">
              <div>自己紹介</div>
              <div>自己紹介</div>
              <div>自己紹介</div>
              <div>自己紹介</div>
            </v-card-text>
          </v-card>
        </v-flex>
        <v-flex xs12>
          <v-card dark color="primary">
            <v-card-text class="px-0">使用技術</v-card-text>
          </v-card>
        </v-flex>
        <v-flex xs12>
          <v-card dark color="primary">
            <v-card-text class="px-0">アピールポイント</v-card-text>
          </v-card>
        </v-flex>
      </v-layout>
    </v-container>
  </div>
</template>
