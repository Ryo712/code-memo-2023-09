<template>
  <div class="text-center">
    <v-btn
      append-icon="mdi-open-in-new"
      color="deep-purple-accent-4"
      @click="overlay = !overlay"
    >
      Launch Application
    </v-btn>
<!--ボタンがクリックされたときに overlay データプロパティをトグルすることで、オーバーレイの表示/非表示を切り替えます。-->
    <v-overlay
      :model-value="overlay"
      class="align-center justify-center"
    >
      <v-progress-circular
        color="primary"
        indeterminate
        size="64"
      ></v-progress-circular>
    </v-overlay>
<!--<v-overlay>: 同じく Vuetify のコンポーネントで、指定された条件
（ここでは :model-value プロパティに overlay データプロパティをバインドしています）が真の場合にオーバーレイを表示します。
このオーバーレイには <v-progress-circular> というプログレスサークルが含まれており、
indeterminate プロパティが設定されているため、回転するプログレスアニメーションが表示されます。-->
  </div>
</template>

<script setup>
  import { ref, watch } from 'vue'

  const overlay = ref(false)
  watch(overlay, val => {
    val && setTimeout(() => {
      overlay.value = false
    }, 3000)
  })
</script>
<!--watch(overlay, val => { ... }): overlay の変更を監視し、値が true に変更された場合、
3秒後に overlay を再び false に設定します。つまり、ボタンがクリックされた後、3秒経つとオーバーレイが非表示になります。-->
<script>
  export default {
    data: () => ({
      overlay: false,
    }),

    watch: {
      overlay (val) {
        val && setTimeout(() => {
          this.overlay = false
        }, 3000)
      },
    },
  }
</script>
<!--watch オプションにも overlay の監視が設定されており、値が true に変更された場合に同様の挙動を行います。-->
<!--このコードはVuetify を使用して、ボタンクリック時にオーバーレイとプログレスサークルを表示し、
一定の時間経過後にそれらを非表示にするシンプルな機能を持つウェブアプリケーションを構築するためのものです。-->