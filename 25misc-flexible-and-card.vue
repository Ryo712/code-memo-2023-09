<template>
  <v-card flat>
    <v-toolbar
      color="primary"
      dark
      extended
      flat
    >
      <v-app-bar-nav-icon></v-app-bar-nav-icon>
    </v-toolbar>
<!--<v-app-bar-nav-icon>: ツールバー内に表示されるアイコンボタンです。
通常、メニューやサイドバーナビゲーションをトグルするために使用されます。-->
    <v-card
      class="mx-auto"
      max-width="700"
      style="margin-top: -64px;"
    >
      <v-toolbar flat>
        <v-toolbar-title class="text-grey">
          Title
        </v-toolbar-title>

        <v-spacer></v-spacer>

        <v-btn icon>
          <v-icon>mdi-magnify</v-icon>
        </v-btn>

        <v-btn icon>
          <v-icon>mdi-apps</v-icon>
        </v-btn>

        <v-btn icon>
          <v-icon>mdi-dots-vertical</v-icon>
        </v-btn>
      </v-toolbar>
<!--<v-btn>:アイコンボタンで、検索アイコン（mdi-magnify）、アプリケーションアイコン（mdi-apps）、
および垂直ドットメニューアイコン（mdi-dots-vertical）が表示されます。-->
      <v-divider></v-divider>

      <v-card-text style="height: 200px;"></v-card-text>
<!--style 属性を使用して高さを200ピクセルに設定していますが、この部分には具体的なテキストは含まれていません。-->
    </v-card>
  </v-card>
</template>