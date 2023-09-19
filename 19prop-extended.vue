<template>
  <v-card
    color="grey-lighten-4"
    flat
    height="200px"
    rounded="0" 
  >
<!-- カードの角を丸めずに設定 -->
    <v-toolbar extended>
      <v-app-bar-nav-icon></v-app-bar-nav-icon>
<!--これはVuetifyのアイコンボタンコンポーネントで、ツールバー内でよく使用されます。
このコンポーネントは通常、メニューやサイドバーを開くトリガーとして使用されます。-->
      <v-toolbar-title>Title</v-toolbar-title>

      <v-spacer></v-spacer>
<!-- ボタンを表示するためのv-btnコンポーネントを使用 -->
      <v-btn icon>
        <v-icon>mdi-magnify</v-icon>
      </v-btn>

      <v-btn icon>
        <v-icon>mdi-heart</v-icon>
      </v-btn>

      <v-btn icon>
        <v-icon>mdi-dots-vertical</v-icon>
      </v-btn>
    </v-toolbar>
  </v-card>
</template>