<template>
  <div class="d-flex justify-center">
    <v-btn>
      Close

      <v-overlay
        activator="parent"
        location-strategy="connected"
        scroll-strategy="close"
      >
<!-- scroll-strategy="close": オーバーレイ内でスクロールが行われるとオーバーレイが自動的に閉じられるように設定しています。
つまり、オーバーレイ内でスクロールしてもオーバーレイが開いたままであり、オーバーレイ内のコンテンツが表示されるだけで、
オーバーレイを閉じるためにはユーザーが明示的に閉じる操作をする必要があります。-->
        <v-card class="pa-2">
          Hello!
        </v-card>
      </v-overlay>
    </v-btn>
  </div>
</template>
<!--ボタンクリックで表示されるオーバーレイを持つコンポーネントを定義。
オーバーレイはボタンに連結されて位置し、コンテンツのスクロールを行うと自動的に閉じられません。
オーバーレイを閉じるためにはユーザーが閉じる操作をすることが必要。-->