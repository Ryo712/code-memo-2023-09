<template>
  <v-card flat>
    <v-container fluid> <!--fluid 属性はコンテナをフル幅に拡張します。-->
      <v-row class="child-flex">
        <div>
          <v-toolbar>
            <v-btn
              icon
              class="hidden-xs-only"
            >
              <v-icon>mdi-arrow-left</v-icon> <!--戻るアイコンの表示-->
            </v-btn>

            <v-toolbar-title>Title</v-toolbar-title> <!--タイトルを表す-->

            <v-spacer></v-spacer>

            <v-btn
              icon
              class="hidden-xs-only"
            >
              <v-icon>mdi-magnify</v-icon> <!--検索アイコンの表示-->
            </v-btn>
          </v-toolbar>
        </div>

        <div style="flex-basis: 20%">
          <v-toolbar dark>
            <v-spacer></v-spacer>

            <v-btn icon>
              <v-icon>mdi-reply</v-icon> <!--戻るボタンを表示-->
            </v-btn>

            <v-btn icon>
              <v-icon>mdi-dots-vertical</v-icon> <!--垂直ドットのメニューを表示-->
            </v-btn>
          </v-toolbar>
        </div>
      </v-row>
    </v-container>
  </v-card>
</template>