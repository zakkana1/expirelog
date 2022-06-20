<template>
  <fieldset>
    <legend>Supplement Info</legend>
    <FormKit
      type="text"
      name="upc"
      label="UPC"
      help="Product UPC"
      validation="required|matches:/^[0-9]{12}/"
      @change="updateField"
    />
    <FormKit
      type="text"
      name="brand"
      label="Brand"
      help="Supplement Brand"
      validation="required"
    />
    <FormKit
      type="text"
      name="name"
      label="Name"
      help="Name of the Supplement"
      validation="required"
    />
    <FormKit
      type="number"
      name="size"
      label="Size"
      help="How many capsules, ounces, grams, etc. are in the bottle"
      validation="required"
    />
    <FormKit
      type="select"
      name="units"
      label="Units"
      help="Unit of measurement used to describe size"
      validation="required"
    />
    <FormKit
      type="number"
      name="doses"
      label="Doses"
      help="How many of the minimum label doses are in the bottle"
    />
    <FormKit
      type="number"
      name="dailydoses"
      label="Doses per Day"
      help="How many of the minimum doses are taken per day"
      validation="required"
    />
  </fieldset>
  <pre wrap>{{ suppInfo }}</pre>
</template>

<script>
// import { ref } from 'vue'

export default {
  name: 'SupplementInfo',
  props: [
    'suppInfo',
    'suppExists'
  ],
  emits: ['field-updated'],
  data () {
    return {

    }
  },
  methods: {
    updateField () {
      this.$emit('field-updated')
    }
  },
  watch: {

  }
}
</script>

<style scoped>
</style>
