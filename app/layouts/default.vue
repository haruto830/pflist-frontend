<template>
  <v-app>
    <v-toolbar>
      <v-toolbar-title
        >pflist
        <span style="font-size:14px;"
          >駆け出したいエンジニアに再び光を</span
        ></v-toolbar-title
      >
      <v-spacer></v-spacer>
      <v-toolbar-items>
        <v-btn flat>ログイン</v-btn>
      </v-toolbar-items>
    </v-toolbar>
    <v-content>
      <v-container>
        <nuxt />
      </v-container>
    </v-content>
    <span>&copy; 2019</span>
  </v-app>
</template>

<script>
export default {}
</script>
