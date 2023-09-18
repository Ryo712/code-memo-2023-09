<template>
  <v-card
    color="grey-lighten-4"
    flat
    height="200px"
    rounded="0"
  >
    <v-toolbar density="compact">
      <v-app-bar-nav-icon></v-app-bar-nav-icon>
<!-- <v-toolbar density="compact">ツールバーコンポーネントを表します。ここでは density="compact" 属性が指定されており、
ツールバーはコンパクトなスタイルで表示されます。通常のツールバーと比較してアイコンやテキストのサイズが小さくなります。-->
      <v-toolbar-title>Title</v-toolbar-title>

      <v-spacer></v-spacer>

      <v-btn icon>
        <v-icon>mdi-magnify</v-icon>
      </v-btn>
<!--ボタン内に表示されるアイコンコンポーネント。これは検索アイコンを示します。-->
      <v-btn icon>
        <v-icon>mdi-heart</v-icon>
      </v-btn>
<!--これはハート（お気に入りなど）を示します。-->
      <v-btn icon>
        <v-icon>mdi-dots-vertical</v-icon>
      </v-btn>
<!--これは垂直方向のドット（メニューアイコンなど）を示します。-->
    </v-toolbar>
  </v-card>
</template>
<!--コンパクトなスタイルのツールバーを備えたカード内のUIコンポーネントを作成するためのものです。
アプリケーションのタイトルやアイコンボタンを含むカードが表示され、ユーザーにさまざまな操作オプションを提供します。-->





