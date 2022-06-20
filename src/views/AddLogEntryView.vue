<template>
  <div id="log-entry-form">
    <h1>Log Entry Form Goes Here</h1>
    <FormKit
      type="form"
      v-model="formData"
      submit-label="Add to Log"
      @submit="formHandler"
    >
      <SupplementInfo :suppInfo="suppInfo" :suppExists="suppExists" @field-updated="fieldUpdated" />
    </FormKit>
  </div>
</template>

<script>
import SupplementInfo from '@/components/SupplementInfo'

export default {
  name: 'AddLogEntryView',
  components: { SupplementInfo },
  data: function () {
    return {
      formData: {},
      suppInfo: {},
      suppExists: false
    }
  },
  methods: {
    formHandler (supplementInfo) {
      console.log('Form Submitted...')
    },
    fieldUpdated () {
      console.log('field updated with:')
    }
  }
}
</script>

<style scoped>

</style>
