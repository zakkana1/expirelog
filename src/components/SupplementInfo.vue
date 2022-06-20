<template>
  <fieldset>
    <legend>Supplement Info</legend>
    <FormKit
      type="text"
      name="upc"
      label="UPC"
      help="Product UPC"
      validation="required|matches:/^[0-9]{12}/"
      @change="updateField('upc')"
    />
    <FormKit
      type="text"
      name="brand"
      label="Brand"
      help="Supplement Brand"
      validation="required"
      @change="updateField('brand')"
    />
    <FormKit
      type="text"
      name="name"
      label="Name"
      help="Name of the Supplement"
      validation="required"
      @change="updateField('name')"
    />
    <FormKit
      type="number"
      name="size"
      label="Size"
      help="How many capsules, ounces, grams, etc. are in the bottle"
      validation="required"
      @change="updateField('size')"
    />
    <FormKit
      type="select"
      :options="unitOptions"
      name="units"
      label="Units"
      help="Unit of measurement used to describe size"
      validation="required"
      @change="updateField('units')"
    />
    <FormKit
      type="number"
      name="doses"
      label="Doses"
      help="How many of the minimum label doses are in the bottle"
      @change="updateField('doses')"
    />
    <FormKit
      type="number"
      name="dailydoses"
      label="Doses per Day"
      help="How many of the minimum doses are taken per day"
      validation="required"
      @change="updateField('dailydoses')"
    />
  </fieldset>
</template>

<script>
// import { ref } from 'vue'

export default {
  name: 'SupplementInfo',
  props: [
    'formData',
    'suppInfo',
    'suppExists'
  ],
  emits: ['field-updated'],
  data () {
    return {
      unitOptions: {
        caps: 'Capsules',
        foz: 'Fluid Ounces',
        woz: 'Ounces'
      }
    }
  },
  methods: {
    updateField (field) {
      console.log(field)
      this.$props.suppInfo.field = this.$props.formData.field
      this.$emit('field-updated')
    }
  },
  watch: {

  }
}
</script>

<style scoped>
</style>
