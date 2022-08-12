<template>
  <div>
    <div class="fromsource">
      <b-form-select v-model="fr_selected" :options="options"></b-form-select>
      <b-button v-b-tooltip.hover title="Test connection" variant="primary">Test</b-button>
    </div>

    <div class="fromsource">
      <b-form-select v-model="to_selected" :options="options"></b-form-select>
      <b-button v-b-tooltip.hover title="Test connection" variant="primary">Test</b-button>
    </div>

    <div class="fromsource">
      <h1>Your cost to move: $3.75</h1>
      <b-button variant="success">Move my data, Hoser!</b-button>
      <b-progress :value="value" :max="max" show-progress animated></b-progress>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HoserMain',
  props: {
    msg: String
  },
    data() {
      return {
        fr_selected: null,
        to_selected: null,
        options: [
          {value: null, text: 'Select...'},
          {value: 'S3', text: 'Amazon S3'},
          {value: 'AzureBlob', text: 'Azure Blob Storage'},
          {value: 'GCS', text: 'Google Cloud Storage', disabled: true},
          {value: 'Vultr', text: 'Vultr Block Storage', disabled: true},
          {value: 'Linode', text: 'Linode Block Storage', disabled: true}
        ],
        value: 45,
        max: 100
      }
  },
  methods: {
    randomValue() {
      this.value = Math.random() * this.max
    }
  }
}
</script>

<style>
.fromsource {
  padding: 1rem;
  margine: 1rem
}
</style>