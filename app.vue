<template>
  <div>
    <!-- <NuxtWelcome /> -->
    Faz apps, implement vue select    
    <v-select
    v-model="selected"
    :options="kampus"
    :reduce="(item) => item.name"
    label="name"
  ></v-select>

  yang dipilih: {{ selected }}

  </div>
</template>

<script>
  import vSelect from 'vue-select';
  import 'vue-select/dist/vue-select.css';
  export default {
    components: [vSelect],
    data() {
      return {
        selected: null,
        kampus: [
          {code: 'lpkia', name: 'LPKIA'},
          {code: 'unisba', name: 'Unisba'},
          {code: 'itb', name: 'ITB'},
          {code: 'upi', name: 'UPI'},
          {code: 'stttelkom', name: 'STT Telkom'},
        ]
      }
    }
  }
  </script>