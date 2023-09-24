<template>
  <v-card
    max-width="500"
    class="mx-auto"
  >
    <v-toolbar
      :color="selection.length ? 'grey darken-4' : 'deep-purple accent-4'"
      dark
    >
<!--タグ: ツールバーコンポーネントです。:color 属性を使用して背景色を動的に設定しており、
選択されたアイテムがある場合はグレー、それ以外の場合は深紫に設定されます。-->
      <v-app-bar-nav-icon v-if="!selection.length"></v-app-bar-nav-icon>
      <v-btn
        v-else
        icon
        @click="selection = []"
      >
        <v-icon>mdi-close</v-icon>
      </v-btn>

      <v-toolbar-title>
        {{ selection.length ? `${selection.length} selected` : 'Photos' }}
      </v-toolbar-title>
<!--ツールバー内に表示されるタイトルです。選択したアイテムがある場合、選択されたアイテムの数が表示され、それ以外の場合は "Photos" と表示されます。-->
      <v-spacer></v-spacer>

      <v-scale-transition>
        <v-btn
          v-if="selection.length"
          key="export"
          icon
        >
          <v-icon>mdi-export-variant</v-icon>
        </v-btn>
      </v-scale-transition>
      <v-scale-transition>
        <v-btn
          v-if="selection.length"
          key="delete"
          icon
        >
<!--アイコンボタンで、選択したアイテムがある場合に表示されます。"export" と "delete" ボタンがあり、それぞれ異なるアイコンが表示されます。-->
          <v-icon>mdi-delete</v-icon>
        </v-btn>
      </v-scale-transition>

      <v-btn icon>
        <v-icon>mdi-dots-vertical</v-icon>
      </v-btn>
    </v-toolbar>

    <v-card-text>
      <v-select
        v-model="selection"
        :items="items"
        multiple
        label="Select an option"
      ></v-select>
    </v-card-text>
  </v-card>
</template>

<script setup>
  import { ref } from 'vue'

  const items = ['Foo', 'Bar', 'Fizz', 'Buzz']

  const selection = ref([])
</script>
<!--const items:選択肢の配列を定義しています。
const selection:selection という変数に割り当て、その初期値として空の配列を持たせるコード。
このリアクティブな変数を使用すると、変数の値が変更されたときにVueが自動的に再レンダリングをトリガーすることができます。-->
<script>
  export default {
    data: () => ({
      selection: [],
      items: ['Foo', 'Bar', 'Fizz', 'Buzz'],
    }),
  }
</script>