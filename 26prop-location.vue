<template>
  <div class="d-flex justify-space-around">
    <v-btn>
      Start
      <v-tooltip
        activator="parent"
        location="start"
      >Tooltip</v-tooltip>
    </v-btn>

    <v-btn>
      End
      <v-tooltip
        activator="parent"
        location="end"
      >Tooltip</v-tooltip>
    </v-btn>

    <v-btn>
      Top
      <v-tooltip
        activator="parent"
        location="top"
      >Tooltip</v-tooltip>
    </v-btn>

    <v-btn>
      Bottom
      <v-tooltip
        activator="parent"
        location="bottom"
      >Tooltip</v-tooltip>
    </v-btn>
<!--・<v-btn> タグに対応する <v-tooltip> タグがあり、それぞれのボタンに対するツールチップを設定します。
    ・ツールチップの activator プロパティは、ツールチップを表示するトリガーとなる要素を指定します。
    ここでは "parent" が指定されており、親要素であるボタンがトリガーとして使用されます。
    ・location プロパティはツールチップの表示位置を指定します。"start"、"end"、"top"、"bottom" 
    それぞれのボタンに対して異なる位置（左、右、上、下）にツールチップが表示されるように設定されています。-->
  </div>
</template>
<!--ボタンをクリックまたはホバーすると、対応する位置にツールチップが表示される単純なUIを作成します。-->