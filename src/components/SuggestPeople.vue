<template>
    <v-list three-line>
        <v-subheader>Who to follow</v-subheader>
        <template v-for="(suggest, index) in suggests">
        <v-divider
            v-if="suggest.divider"
            :inset="suggest.inset"
            :key="index"
        ></v-divider>

        <v-list-tile
            v-else
            :key="index"
            avatar
        >
            <v-list-tile-avatar>
            <img :src="suggest.avatar">
            </v-list-tile-avatar>

            <v-list-tile-content>
            <v-list-tile-title v-html="suggest.title"></v-list-tile-title>
            <v-list-tile-sub-title v-html="suggest.subtitle"></v-list-tile-sub-title>
            </v-list-tile-content>
            <v-btn small outline color="blue lighten-1" dark>Follow</v-btn>
        </v-list-tile>
        </template>
    </v-list>
</template>

<script>
  export default {
    data () {
      return {
        suggests: [
          {
            avatar: 'https://cdn.vuetifyjs.com/images/lists/1.jpg',
            title: 'John Leider',
            subtitle: "I once wrote a song about this avatar."
          },
          { divider: true, inset: true },
          {
            avatar: 'https://cdn.vuetifyjs.com/images/lists/2.jpg',
            title: 'Lenai',
            subtitle: "Hello World."
          },
          { divider: true, inset: true },
          {
            avatar: 'https://cdn.vuetifyjs.com/images/lists/3.jpg',
            title: 'Despcae Lino',
            subtitle: "Welcome to Vuetify.js!"
          }
        ]
      }
    }
  }
</script>
