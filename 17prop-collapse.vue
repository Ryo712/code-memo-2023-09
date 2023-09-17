<template>
  <v-card
    color="grey-lighten-4"
    flat
    height="200px"
    rounded="0"
  >
    <v-toolbar collapse>
      <v-btn icon>
        <v-icon>mdi-magnify</v-icon>
      </v-btn>
<!--<v-toolbar collapse>: ツールバーコンポーネントを表します。ここでは collapse 属性が指定されており、ツールバーはデフォルトで折りたたまれた状態です。-->
<!--<v-icon>: ボタン内に表示されるアイコンコンポーネントです。ここでは「mdi-magnify」アイコンが指定されており、
これは検索アイコンを示します。検索機能へのリンクまたはトリガーに使用されることが一般的です-->
      <v-btn icon>
        <v-icon>mdi-dots-vertical</v-icon>
      </v-btn>
    </v-toolbar>
  </v-card>
</template>
<!--ここでは「mdi-dots-vertical」アイコンが指定されており、これは垂直方向のドット（メニューアイコンなど）を示します。-->