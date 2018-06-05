<template>
  <v-card>
    <v-card-media :src="image" height="200"/>
    <v-card-title primary-title class="text-xs-left">{{ text }}</v-card-title>
    <v-card-text class="text-xs-right">{{ formatTime }}</v-card-text>
  </v-card>
</template>

<script>
import moment from 'moment';

export default {
  name: 'ListItem',
  props: [
    'image',
    'text',
    'datetime',
  ],
  computed: {
    formatTime() {
      return moment.unix(this.datetime).format('ddd, DD MMM YYYY HH:mm');
    },
  },
};
</script>

<style scoped>

</style>
