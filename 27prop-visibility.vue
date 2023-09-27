<template>
  <v-container
    fluid
    class="text-center"
  >
<!--fluid クラスが指定されています。fluid クラスは、コンテナの幅を親要素に合わせるために使用されます。-->
    <v-row
      class="flex"
      justify="space-between"
    >
      <v-col cols="12">
        <v-btn @click="show = !show">
          toggle
        </v-btn>
      </v-col>
<!--cols="12" は列が12つのカラムを占有することを示します。
クリック時に show の値をトグルするための @click イベントリスナーが設定されています。-->
      <v-col
        cols="12"
        class="mt-12"
      >
        <v-tooltip
          v-model="show"
          location="top"
        >
<!--Vuetify のツールチップコンポーネントで、プログラム的に表示/非表示を切り替えるための v-model ディレクティブが 
show にバインドされています。ツールチップの表示位置は location="top"。-->
          <template v-slot:activator="{ props }">
            <v-btn
              icon
              v-bind="props"
            >
<!--ツールチップのトリガーとなるアクティベーター（トリガー要素）を指定します。v-btn 内のアイコンボタンがトリガーとして機能し、
v-bind="props" によりアクティベーターのプロパティが適用されます。-->
              <v-icon color="grey-lighten-1">
                mdi-cart
              </v-icon>
            </v-btn>
          </template>
          <span>Programmatic tooltip</span>
        </v-tooltip>
      </v-col>
    </v-row>
  </v-container>
</template>

<script setup>
  import { ref } from 'vue'

  const show = ref(false)
</script>
<!--コンポーネントのロジックが含まれる。
ref 関数を使用して show のリアクティブデータを定義し、トグル可能な状態を管理します。-->
<script>
  export default {
    data () {
      return {
        show: false,
      }
    },
  }
</script>
<!--ボタンをクリックすることで show の値が切り替わり、それに応じてツールチップが表示または非表示になります。-->