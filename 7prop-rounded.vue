<template>
  <v-container>
    <v-row justify="space-around">
      <v-col
        v-for="rounded in [false, true, 'xl']"
        :key="String(rounded)"
        cols="12"
        md="4"
      >
<!--<v-col>: グリッド内の各列を表す要素です。v-for ディレクティブを使用して、rounded 配列内の各要素に対してループします。-->
        <v-sheet
          class="pa-12"
          color="grey-lighten-3"
        >
          <div></div>
<!--<div></div>: 空の <div> 要素がシート内に配置されており、シートの上と下に余白を設定するために使用されます。-->
          <v-sheet
            :rounded="rounded"
            class="mx-auto"
            height="100"
            width="100"
          ></v-sheet>
<!--:rounded プロパティを設定して、各シートの角丸設定を指定します。rounded 配列内の値（false, true, 'xl'）に応じて、角丸の具合が異なります。
rounded が false の場合は角丸がなく、true の場合は標準の角丸が適用され、'xl' の場合は大きな角丸が適用されます。
height と width プロパティを使用して、各シートの高さと幅を100ピクセルに設定します。-->
          <div></div>
        </v-sheet>
      </v-col>
    </v-row>
  </v-container>
</template>
<!--異なる角丸設定を持つボックスを表示するシンプルなウェブアプリケーションを構築するためのものです。
rounded 配列内の異なる値を使って、角丸の具合を調整し、ページ上に表示します。-->