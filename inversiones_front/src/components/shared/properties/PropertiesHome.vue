<template>
  <v-tabs
    centered
    color="primary"
    dark
    icons-and-text
  >
    <v-tabs-slider color="#95c41f"></v-tabs-slider>

    <v-tab href="#tab-1" @click="rent">
      Arriendos
      <v-icon>phone</v-icon>
    </v-tab>

    <v-tab href="#tab-2" @click="sale">
      Ventas
      <v-icon>favorite</v-icon>
    </v-tab>

    <v-tab href="#tab-3" @click="franquicia">
      Inversiones
      <v-icon>account_box</v-icon>
    </v-tab>

    <v-tab-item
      v-for="i in 3"
      :key="i"
      :value="'tab-' + i"
    >
      <v-card flat>
        <v-card-text>{{ text }}</v-card-text>
      </v-card>
    </v-tab-item>
  </v-tabs>
</template>
<script>
  export default {
    data () {
      return {
        model: 'tab-1',
        text: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.'
      }
    },
    methods: {
        rent() {
            alert('Arriendos')
        },
        sale() {
            alert('Ventas')
        },
        franquicia() {
            alert('Franquicias')
        }
    }
  }
</script>