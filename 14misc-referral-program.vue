<template>
  <v-sheet
    border="lg opacity-12"
    class="text-body-2 mx-auto"
    max-width="550"
  >
    <v-container fluid>
      <v-row>
        <v-col cols="12" md="3">
          <v-img src="https://cdn.vuetifyjs.com/docs/images/graphics/img-placeholder.png" height="88" cover></v-img>
        </v-col>
<!--グリッド内の1つ目の列を定義します。スマートフォンサイズ (cols="12") および中サイズ (md="3") のレイアウトに対応しています。-->
        <v-col cols="12" md="9">
          <p class="mb-4">
            This is part of our <a href="#">Most Comprehenseive Guide to Referral Programs</a> > <a href="#">Do I Need A Referral Program?</a> section. You may enjoy other related articles:
          </p>
<!--グリッド内の2つ目の列を定義します。スマートフォンサイズ (cols="12") および中サイズ (md="9") のレイアウトに対応しています。-->
          <ul class="ps-4 mb-6">
            <li>
              <a href="#">5 Ways to See if Referral Programs Can Work for You</a>
            </li>
            <li>
              <a href="#">The 6 Key Benefits of Referral Marketing</a>
            </li>
            <li>
              <a href="#">Leading Indicators of Referral Program Success</a>
            </li>
            <li>
              <a href="#">Debunking the Top 5 Worst Referral Program Myths</a>
            </li>
          </ul>

          <v-btn
            block
            class="text-none"
            color="info"
            rounded="0"
            variant="flat"
          >
            <span class="hidden-sm-and-down">
              Explore our 38+ Referral Program Resources
            </span>

            <span class="hidden-md-and-up">
              Explore Referral Resources
            </span>
          </v-btn>
<!--<v-btn>:Vuetifyのボタンコンポーネント。2つのボタンが定義されている。Explore our 38+ Referral Program Resources」ボタン: テキストは大画面用と小画面用で異なり、
大画面では「Explore our 38+ Referral Program Resources」と表示され、小画面では「Explore Referral Resources」と表示されます。-->
        </v-col>
      </v-row>
    </v-container>
  </v-sheet>
</template>