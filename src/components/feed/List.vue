<template>
  <v-container fluid grid-list-lg>
    <v-layout row wrap>
      <v-flex v-for="feed in feeds" :key="feed.id" xs12 md6 offset-md3>
        <v-card >
          <v-card-media :src="feed.image" height="200" />
          <v-card-title primary-title class="text-xs-left">{{ feed.text }}</v-card-title>
        </v-card>
      </v-flex>
    </v-layout>
  </v-container>
</template>


<script>
export default {
  name: 'List',
  computed: {
    feeds() {
      return [
        {
          id: 1,
          image: 'https://images.unsplash.com/photo-1520716497194-0bde97ce9abe?ixlib=rb-0.3.5&ixid=eyJhcHBfaWQiOjEyMDd9&s=c8936d0802da9d0b3554637661201471&auto=format&fit=crop&w=701&q=80',
          text: '1 Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum is simply dummy text of the printing and typesetting industry.',
          datetime: 1519295400,
        },
        {
          id: 2,
          image: 'https://images.unsplash.com/photo-1520704103437-2b033fcfa64f?ixlib=rb-0.3.5&ixid=eyJhcHBfaWQiOjEyMDd9&s=595bd894ef85d6c8fbbb24e210635710&auto=format&fit=crop&w=564&q=80',
          text: '2 Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum is simply dummy text of the printing and typesetting industry.',
          datetime: 1519299000,
        },
        {
          id: 3,
          image: 'https://images.unsplash.com/photo-1520722217742-5887a8cb5778?ixlib=rb-0.3.5&ixid=eyJhcHBfaWQiOjEyMDd9&s=6e82e7e3dd060b43c1301238185b12b5&auto=format&fit=crop&w=634&q=80',
          text: '3 Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum is simply dummy text of the printing and typesetting industry.',
          datetime: 1519381800,
        },
      ];
    },
  },
};
</script>

<style scoped>

</style>
