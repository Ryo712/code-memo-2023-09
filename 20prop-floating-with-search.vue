<template>
  <v-card
    class="pa-4"
    flat
    height="300px"
    img="https://cdn.vuetifyjs.com/images/toolbar/map.jpg"
  >
<!--class:クラス属性を指定し、カードにスタイリングを適用します。
    flat:カードのデザインをフラットにし、影を削除します。-->
    <v-toolbar
      dense
      floating
    >
<!--dense:ツールバーのコンパクト表示モードを有効にします。
    float:ツールバーを浮動表示にします。-->
      <v-text-field
        hide-details
        prepend-icon="mdi-magnify"
        single-line
      ></v-text-field>

      <v-btn icon>
        <v-icon>mdi-crosshairs-gps</v-icon>
      </v-btn>

      <v-btn icon>
        <v-icon>mdi-dots-vertical</v-icon>
      </v-btn>
    </v-toolbar>
  </v-card>
</template>
<!--このコードの目的は、Vuetifyのコンポーネントを組み合わせて、カード内にテキスト入力フィールド、
アイコンボタン、および背景画像を配置することです。-->