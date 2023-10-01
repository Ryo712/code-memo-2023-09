<template>
  <div>
    <v-file-input
      chips
      multiple
      label="File input w/ chips"
    ></v-file-input>
<!--chips: ファイルの選択後、ファイル名が表示される「チップ」（小さな表示要素）を有効にします。選択したファイルが表示されます。
    multiple: 複数のファイルを選択できるようにします。
    ラベルは "File input w/ chips"です。-->
    <v-file-input
      small-chips
      multiple
      label="File input w/ small chips"
    ></v-file-input>
  </div>
</template>