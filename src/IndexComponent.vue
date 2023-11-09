<template>
  <div v-html="htmlContent"></div>
</template>

<script>
export default {
  data() {
    return {
      htmlContent: ''
    }
  },
  async mounted() {
    const response = await fetch('/path/to/index.html')
    this.htmlContent = await response.text()
  }
}
</script>