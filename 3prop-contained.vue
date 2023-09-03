<template>
  <v-row
    align="center"
    class="ma-4"
    justify="center"
  >
    <v-card
      height="300"
      width="250"
    >
      <v-row justify="center">
        <v-btn
          color="success"
          class="mt-12"
          @click="overlay = !overlay"
        >
          Show Overlay
        </v-btn>

        <v-overlay
          v-model="overlay"
          contained
          class="align-center justify-center"
        >
<!--<v-overlay>:オーバーレイ（モーダルウィンドウ）を定義し、v-modelディレクティブを使用して表示状態を制御しています。
ボタンをクリックすると、このオーバーレイが表示または非表示になります。-->
          <v-btn
            color="success"
            @click="overlay = false"
          >
            Hide Overlay
          </v-btn>
        </v-overlay>
      </v-row>
    </v-card>
  </v-row>
</template>

<script setup>
  import { ref } from 'vue'

  const overlay = ref(false)
</script>
<!--const overlay = ref(false): overlay というリアクティブな変数を定義し、
初期値を false に設定しています。この変数はオーバーレイの表示状態を追跡します。-->
<script>
  export default {
    data: () => ({
      overlay: false,
    }),
  }
/*data オプション: オーバーレイの表示状態を管理するためのデータプロパティ overlay を定義しています。*/
</script>
<!--オーバーレイの表示状態は、overlay 変数を介して制御されます。
Vue.jsのリアクティビティシステムによって、overlay の値が変更されると、オーバーレイの表示状態が自動的に変更されます。-->
<!--要点：このコードでは、overlay という変数がリアクティビティシステムによって監視されています。
つまり、overlay の値が変更されると、Vue.jsはそれを検知し、オーバーレイの表示状態を自動的に変更します。-->
