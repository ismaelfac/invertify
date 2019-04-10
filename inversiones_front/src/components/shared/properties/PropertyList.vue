<template>
  <v-hover>
    <v-card
      slot-scope="{ hover }"
      class="mx-auto"
      color="grey lighten-4"
      max-width="300"
    >
      <v-img :aspect-ratio="16/9" src="https://cdn.vuetifyjs.com/images/cards/kitchen.png">
        <v-expand-transition>
          <div
            v-if="hover"
            class="d-flex transition-fast-in-fast-out grey darken-2 v-card--reveal display-3 white--text"
            style="height: 100%;"
          >
          <div class="text-xs-center">
          <v-btn outline color="#fff" v-if="hover" class="btn_details"><router-link to="property">Detalles</router-link></v-btn>
          </div>
          </div>
        </v-expand-transition>
        
      </v-img>
      <v-footer height="auto" color="primary lighten-1">
        <v-layout justify-center row wrap>
        <v-btn v-for="icon in icons" :key="icon.id" write icon>
          <v-icon large color="blue-grey">mdi-{{ icon.icon }}</v-icon><strong>{{ icon.cant}} </strong>
        </v-btn>
        </v-layout>
      </v-footer>
      <v-card-text class="pt-4" style="position: relative;">        
        <div class="font-weight-light grey--text title mb-2">For the perfect meal</div>
      </v-card-text>
    </v-card>
  </v-hover>
</template>
<script>
export default {
    name: 'PropertyList',
    data: () => ({
      icons: [
        {'id': 1,'icon':'grid-large', 'cant':'345'},
        {'id': 2,'icon':'hotel', 'cant':'2'},
        {'id': 3,'icon':'shower', 'cant':'2'},
        {'id': 4,'icon':'office-building', 'cant':'4'}
      ]
    })
}
</script>
<style>
.v-card--reveal {
  align-items: center;
  bottom: 0;
  justify-content: center;
  opacity: .5;
  position: absolute;
  width: 100%;
}
.btn_details{
  color: #95c41f;
}
</style>

