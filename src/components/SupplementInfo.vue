<template>
  <fieldset>
    <legend>Supplement Info</legend>
    <FormKit
      type="text"
      name="upc"
      label="UPC"
      help="Product UPC"
      validation="required"
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
</template>

<script>
// import { ref } from 'vue'

export default {
  name: 'SupplementInfo',
  setup () {
    // const supplementExists = ref(false)
    // const supplementInfo = ref({})
  },
  data () {
    return {

    }
  }
}
</script>

<style scoped>
</style>
