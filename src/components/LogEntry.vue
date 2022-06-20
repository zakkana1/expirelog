<template>
  <fieldset>
    <legend>Log Entry</legend>
    <p>This is line {{ currentLineNumber }} out of {{ lineCount }} lines.</p>
  </fieldset>
</template>

<script>
export default {
  name: 'LogEntry',
  props: [
    'lineCount',
    'currentLineNumber'
  ],
  emits: ['increment-line-count'],
  methods: {
    incrementLineCount (lineCount) {
      lineCount++
      this.$emit('increment-line-count')
    }
  }
}
</script>

<style scoped>

</style>
