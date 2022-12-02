<template>
  <div class="max-width-1300">
    <v-form>
      <v-container>
        <v-row>
          <v-col cols="12">
            <validation-provider v-slot="{ errors }" name="Name" rules="text" vid="name">
              <v-text-field v-model="formData.name" :error-messages="errors" label="Name" dense outlined></v-text-field>
              <p>{{ errors }}</p>
            </validation-provider>
          </v-col>
        </v-row>
        <v-btn>Submit</v-btn>
      </v-container>
    </v-form>
    <button @click="goRoute">go link</button>
  </div>
</template>
<script>
export default {
  data() {
    return {
      email: '',
      lastname: '',
      firstname: '',
      formData: {
        name: '',
      },
    }
  },
  methods: {
    goRoute() {
      const isConfirmd = window.confirm('are you sure')
      if (isConfirmd) {
        this.$router.push('/rastictedroute');
      }
    }
  },
}
</script>
