<template>
  <div class="cf-form-field">
    <input
      class="cf-form-input"
      type="text"
      placeholder="Example"
    />
    <button class="cf-btn-primary">Example Button</button>
  </div>
</template>

<script>
import { init as initContentfulExtension } from 'contentful-ui-extensions-sdk'

export default {
  data () {
    return {
      extension: null
    }
  },
  mounted () {
    initContentfulExtension((extension) => {
      this.extension = extension
      this.extension.window.startAutoResizer()
    })
  }
}
</script>
