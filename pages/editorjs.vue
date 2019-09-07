<template>
  <div class="form-container">
    <h2>Editor.js sample</h2>
    <button @click="save">Save</button>
    <editor
      autofocus
      ref="editor"
      holder-id="codex-editor"
      save-button-id="save-button"
      :init-data="initData"
      @save="save"
      @ready="onReady"
      @change="onChange"
      class="editor"
    />
  </div>
</template>

<script>
import { Editor } from 'vue-editor-js'
import sampleData from '~/modules/sampleData'

export default {
  components: {
    Editor
  },
  created() {
    this.initData = sampleData()
  },
  data() {
    return {
      initData: {}
    }
  },
  methods: {
    save() {
      console.log('save')
      console.log(this.$refs.editor)
      // this.$refs.editor.save() // TODO: 実行すると無限ループになる
    },
    onSave(response) {
      console.log(JSON.stringify(response))
    },
    onReady() {
      console.log('onReady')
    },
    onChange() {
      console.log('onChange')
    }
  }
}
</script>
