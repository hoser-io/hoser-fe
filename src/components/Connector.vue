<template>
  <div>
    <b-form>
      <b-form-group id="input-group-1" label="Provider:" label-for="input-1">
        <b-form-select
          id="input-1"
          v-model="form.provider"
          :options="providers"
          required
        ></b-form-select>
      </b-form-group>

      <b-form-group
        id="input-group-2"
        label="Name:"
        label-for="input-2"
      >
        <b-form-input
          id="input-2"
          v-model="form.name"
          placeholder="Enter block name"
          required
        ></b-form-input>
      </b-form-group>

      <b-form-group 
        id="input-group-3" 
        label="Credential:" 
        label-for="input-3"
      >
        <b-form-input
          id="input-2"
          v-model="form.credential"
          placeholder="Enter credential"
          required
        ></b-form-input>
      </b-form-group>

      <b-button type="test" variant="primary">Test</b-button>
    </b-form>
    <b-card class="mt-3" header="Test Result">
      <pre class="m-0">This could be single test record retrieved</pre>
    </b-card>
  </div>
</template>

<script>
  export default {
    name: 'Connector',
    data() {
      return {
        form: {
          name: '',
          credential: '',
          provider: null
        },
        providers: [
          {value: null, text: 'Select One'},
          {value: 'S3', text: 'Amazon S3'},
          {value: 'AzureBlob', text: 'Azure Blob Storage'},
          {value: 'GCS', text: 'Google Cloud Storage', disabled: true},
          {value: 'Vultr', text: 'Vultr Block Storage', disabled: true},
          {value: 'Linode', text: 'Linode Block Storage', disabled: true}
        ]
      }
    }
  }
</script>