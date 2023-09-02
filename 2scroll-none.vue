<template>
  <div class="d-flex justify-center">
    <v-btn>
      None

      <v-overlay
        activator="parent"
        location-strategy="connected"
        scroll-strategy="none"
      >
<!--・オーバーレイを表示させるために、トリガーとなる要素は「親要素（ボタン）」です。
    ・つまり、ボタンをクリックすると、その親要素であるボタンがオーバーレイの表示をトリガーとします。
    ・scroll-strategy="none"スクロール時のオーバーレイの挙動を指定しています。
    "scroll-strategy" が "none" に設定されている場合、スクロールがオーバーレイに影響を与えないことを示します。(オーバーレイが常に表示されたまま。)-->
        <v-card class="pa-2">
          Hello!
        </v-card>
      </v-overlay>
<!--これは Vuetify オーバーレイコンポーネントです。
オーバーレイは他のコンポーネント（この場合はボタン）の上に重ねて表示され、
ユーザーインタラクションを制御できます。-->
    </v-btn>
  </div>
</template>
<!--template内はVue.js コンポーネント内でHTMLのマークアップ（要素や構造）を定義するための特別なセクション。-->