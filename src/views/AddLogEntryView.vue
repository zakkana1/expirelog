<template>
  <div id="log-entry-form">
    <h1>Log Entry Form Goes Here</h1>
    <FormKit
      type="form"
      v-model="formData"
      submit-label="Add to Log"
      @submit="formHandler"
    >
      <SupplementInfo :formData="formData" :suppInfo="suppInfo" :suppExists="suppExists" />
    </FormKit>
    <pre wrap>{{ formData }}</pre>
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
    }
  }
}
</script>

<style scoped>

</style>
