<template>
  <div class="form-container">
    <h2>Editor.js sample</h2>
    <editor
      autofocus
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
