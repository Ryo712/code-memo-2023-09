<template>
  <v-container>
    <v-row class="flex-child text-subtitle-2">
      <v-col
        class="d-flex"
        cols="12"
        md="4"
      >
<!--<v-col>: グリッド内の各列を表す要素で、ここでは4つの異なる列が定義されています。
各 <v-col> はクラス d-flex を持ち、子要素を横方向に配置します。-->
        <v-sheet
          class="d-flex"
          color="grey-lighten-3"
          height="424"
        >
          <sheet-footer>
            #1: (3r x 2c)
          </sheet-footer>
        </v-sheet>
      </v-col>

      <v-col
        class="d-flex"
        cols="12"
        md="4"
      >
        <v-row class="ma-n3">
          <v-col cols="6">
            <v-sheet
              class="d-flex"
              color="green-lighten-3"
              height="150"
            >
              <sheet-footer>
                #2: (1r x 1c)
              </sheet-footer>
            </v-sheet>
          </v-col>

          <v-col cols="6">
            <v-sheet
              class="d-flex"
              color="yellow-lighten-3"
              height="150"
            >
              <sheet-footer>
                #3: (1r x 1c)
              </sheet-footer>
            </v-sheet>
          </v-col>

          <v-col cols="12">
            <v-sheet
              class="d-flex"
              color="red-lighten-3"
              height="250"
            >
              <sheet-footer>
                #5: (2r x 2c)
              </sheet-footer>
            </v-sheet>
          </v-col>
        </v-row>
      </v-col>

      <v-col
        cols="6"
        md="2"
      >
        <v-sheet
          class="d-flex"
          color="teal-lighten-3"
          height="300"
        >
          <sheet-footer>
            #4: (2r x 1c)
          </sheet-footer>
        </v-sheet>
      </v-col>

      <v-col
        class="d-flex"
        cols="6"
        md="2"
      >
        <v-sheet
          class="d-flex mt-auto"
          color="purple-lighten-3"
          height="300"
        >
          <sheet-footer>
            #6: (2r x 1c)
          </sheet-footer>
        </v-sheet>
      </v-col>
    </v-row>
  </v-container>
</template>

<script setup>
  import { h } from 'vue'
//import { h } from 'vue':Vue 3 の h 関数（仮想DOM要素を作成するための関数）をインポートします。
  const SheetFooter = {
    setup (_, { slots }) {
      return () => h('v-sheet', {
        class: 'ma-auto px-4',
        color: 'rgba(0, 0, 0, .36)',
        height: 50,
      }, slots.default())
    },
  }
</script>
<!--仮想DOMはウェブアプリケーションのUIを効率的に更新するために使用されるテクニックの一部であり、Vue.jsはこの仮想DOMを操作するために h 関数を提供しています。
コンポーネント内で新しい要素を生成したり、変更したりする際に h 関数を使用することで、Vue.jsは変更が必要な部分を特定し、効率的にリアルDOMに反映させることができます。
つまりVueコンポーネント内で動的なUIを生成できるようになります。-->
<script>
  import { h } from 'vue'
// Vue 3 の h 関数を再度インポートします。
  export default {
    components: {
      // A simple helper component
      SheetFooter: {
        setup (_, { slots }) {
          return () => h('v-sheet', {
            class: 'ma-auto px-4',
            color: 'rgba(0, 0, 0, .36)',
            height: 50,
          }, slots.default())
        },
      },
    },
//SheetFooter コンポーネント: カスタムコンポーネントを再度定義し、components オプション内で使用可能にします。//
//<sheet-footer> v-sheet コンポーネント内に配置され、高さが50ピクセルで、背景色が rgba(0, 0, 0, .36) に設定されています。//
  }
</script>
<!--Vuetifyを使用して異なる外観を持つシートを表示し、カスタムコンポーネント SheetFooter を使用して各シートのフッター部分を生成します。
列と行の組み合わせにより、多彩なデザインのシートが構築される-->