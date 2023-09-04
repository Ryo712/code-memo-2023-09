<template>
  <div>
    <v-hover v-slot="{ isHovering, props }">
<!--v-slot="{ isHovering, props }": v-hover コンポーネントは、マウスホバー時の状態を監視し、
その状態を isHovering という変数に保存します。また、カード要素に適用するためのプロパティを 
props という変数に保存します-->
      <v-card
        class="mx-auto"
        max-width="344"
        v-bind="props"
      >
<!--v-bind="props": props 変数の値をカード要素にバインドしています。
これにより、v-hover の設定に従ってカードのプロパティが変更されます。-->
        <v-img src="https://cdn.vuetifyjs.com/images/cards/forest-art.jpg"></v-img>

        <v-card-text>
          <h2 class="text-h6 text-primary">
            Magento Forests
          </h2>
          Travel to the best outdoor experience on planet Earth. A vacation you will never forget!
        </v-card-text>

        <v-card-title>
          <v-rating
            :model-value="4"
            dense
            color="orange"
            background-color="orange"
            hover
            class="me-2"
          ></v-rating>
<!--<v-rating> コンポーネントは星評価を表示し、:model-value プロパティで初期評価を設定しています。-->
          <span class="text-primary text-subtitle-2">64 Reviews</span>
        </v-card-title>

        <v-overlay
          :model-value="isHovering" 
          contained
          scrim="#036358"
          class="align-center justify-center"
        >
<!--isHoveringの値に応じて、マウスホバー時に isHovering が true になると、オーバーレイが表示されます。
contained: オーバーレイがカード内に収まるように制約されることを意味します。-->
          <v-btn variant="flat">See more info</v-btn>
        </v-overlay>
      </v-card>
    </v-hover>
  </div>
</template>
<!--これはマウスホバー時にカードの詳細情報をユーザーに表示する簡単なカードコンポーネントの例です。-->