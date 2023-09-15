<template>
  <div>
<!--uetifyのトップバーまたはナビゲーションバーを表すコンポーネントで以下属性が指定されている。
dark: トップバーのテキストやアイコンが白色で表示されるようにダークモードが有効になっています。
prominent: トップバーが目立つようにスタイルが適用されます。
img:背景に表示されるイメージを指定。-->
    <v-toolbar
      dark
      prominent
      image="https://cdn.vuetifyjs.com/images/backgrounds/vbanner.jpg"
    >
      <v-app-bar-nav-icon></v-app-bar-nav-icon>
<!--ナビゲーションバーの左側に、モバイルデバイスで表示されるハンバーガーアイコン（三本線アイコン）が配置されています。
ハンバーガーアイコンをクリックすると、通常はメニューが表示されます。-->
      <v-toolbar-title>Vuetify</v-toolbar-title>

      <v-spacer></v-spacer>

      <v-btn icon>
        <v-icon>mdi-export</v-icon>
      </v-btn>
    </v-toolbar>
  </div>
</template>
<!--ダークモードを有効にし、目立つトップバーにVuetifyのロゴとアイコンを含む簡単なナビゲーションバーを作成するためのものです。
背景に画像を持ち、ハンバーガーハンバーガーアイコン、エクスポートアイコンのアクセスが提供されている-->