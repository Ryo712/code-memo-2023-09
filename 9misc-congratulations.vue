<template>
  <v-sheet
    class="d-flex align-center justify-center flex-wrap text-center mx-auto px-4"
    elevation="4"
    height="250"
    rounded
    max-width="800"
    width="100%"
  >
<!--<v-sheet>: Vuetifyのコンポーネントで、カードライクな外観を持つコンテナ要素です。
上記のclass,elevation,height,rounded,max-width,width属性が指定されている。-->
    <div>
      <h2 class="text-h4 font-weight-black text-orange">Congratulations!</h2> <!--メッセージタイトル-->

      <div class="text-h5 font-weight-medium mb-2">
        You are officially a part of the Vuetify Community!
      </div> <!--サブメッセージ-->

      <p class="text-body-2 mb-4">
        Please head over to your inbox/spam or others folder to find our verificaiton email.
      </p> <!--メッセージの本文-->

      <v-btn variant="text" color="orange">Go to Login</v-btn>
<!--<v-btn>: Vuetifyのボタンコンポーネントで、テキスト「Go to Login」を表示します。ボタンの色はオレンジに設定されています。-->
    </div>
  </v-sheet>
</template>
<!--Vuetifyを使用して、ユーザーにウェルカムメッセージと次のアクションへのリンクを提供するシンプルなUIコンポーネントを作成するためのものです。
シートはコンテナとして機能し、その内部にテキスト要素とボタンが配置されています。-->