<template>
  <div>
    <v-container grid-list-md text-xs-center>
      <v-card dark class="mx-auto" style="max-width: 500px;">
        <v-text-field label="ポートフォリオ名"></v-text-field>
        <v-text-field label="ポートフォリオURL"></v-text-field>
        <v-text-field label="GitHub URL"></v-text-field>
        <v-textarea label="概要" value="" :counter="255"></v-textarea>
        <v-textarea
          label="アピールポイント"
          value=""
          :counter="1000"
        ></v-textarea>
        <v-text-field label="スキル"></v-text-field>
      </v-card>
    </v-container>
  </div>
</template>
