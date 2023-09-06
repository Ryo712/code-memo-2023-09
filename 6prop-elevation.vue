<template>
  <v-container>
    <v-row justify="space-around">
      <v-col
        v-for="elevation in elevations"
        :key="elevation"
        cols="12"
        md="4"
      >
<!--<v-col>: グリッド内の各列を表す要素です。v-for ディレクティブを使用して、elevations 配列内の各要素に対してループします。-->
        <v-sheet
          class="pa-12"
          color="grey-lighten-3"
        >
          <v-sheet
            :elevation="elevation"
            class="mx-auto"
            height="100"
            width="100"
          ></v-sheet>
<!--<v-sheet :elevation="elevation">: :elevation プロパティを設定して、各シートの影の高さを指定します。
elevation 変数は v-for ループ内で取得され、異なる高さの影を持つシートを作成します。-->
        </v-sheet>
      </v-col>
    </v-row>
  </v-container>
</template>

<script setup>
  const elevations = [0, 4, 8, 12, 16, 20]
</script>
<!--const elevations = [0, 4, 8, 12, 16, 20]: elevations という配列を定義し、それぞれのシートの影の高さを示す値を格納します。-->
<script>
  export default {
    data: () => ({
      elevations: [0, 4, 8, 12, 16, 20],
    }),
  }
</script>
<!--data プロパティ内にも elevations 配列が定義されており、同じく各シートの影の高さを示す値が格納されています。-->
<!--このコードは異なる高さの影を持つボックスを表示するシンプルなウェブアプリケーションを構築するためのものです。
各シートは中央揃えで表示され、グレーの背景色を持っています。影の高さは、elevation プロパティを調整することで変更できます。-->