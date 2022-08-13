<template>
  <b-container>
    <b-row class="m-5">
      <b-col>
        <b-form-select class="m-2" v-model="fr_selected" :options="options"></b-form-select>
        <b-button class="m-2" v-b-tooltip.hover title="Test connection" variant="primary">Test</b-button>
      </b-col>
      <b-col class="justify-content-md-center">
        <b-button @click="randomValue" class="m-2" variant="success">Move my data, Hoser!</b-button>
      </b-col>
      <b-col>
        <b-form-select class="m-2" v-model="to_selected" :options="options"></b-form-select>
        <b-button class="m-2" v-b-tooltip.hover title="Test connection" variant="primary">Test</b-button>
      </b-col>
    </b-row>
    <b-progress class="mx-md-n5" :value="value" :max="max" show-progress animated></b-progress>
  </b-container>
</template>

<script>
export default {
  name: 'HoserMain',
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
        value: 0,
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
