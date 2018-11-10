<template>
    <v-layout row wrap class="mx-3 my-5">
        <template  v-for="(feed, index) in feeds">
            <v-flex xs5 :key="index">
                <p>
                    <v-avatar size="30px" class="mr-1">
                        <img :src="feed.upl_avatar">
                    </v-avatar>
                    {{feed.upl_name}} uploaded
                </p>

                <v-card>
                    <v-img height="200px" :src="feed.cover" class="text-md-center">
                        <v-layout justify-center align-center row fill-height>
                            <v-flex>
                                <v-icon size="72px" color="grey lighten-3" class="btn-cover">play_circle_outline</v-icon>
                            </v-flex>
                        </v-layout>
                    </v-img>
                </v-card>

                <v-card-actions>
                  <v-icon color="grey darken-2">access_time</v-icon>{{feed.upl_time}}

                  <v-spacer></v-spacer>

                  <v-btn icon>
                      <v-icon color="grey darken-2">headset</v-icon>{{feed.listened}}
                  </v-btn>

                  <v-btn icon>
                    <v-icon color="grey darken-2">favorite_border</v-icon>{{feed.liked}}
                  </v-btn>

                  <v-btn icon>
                    <v-icon color="grey darken-2">share</v-icon>{{feed.shared}}
                  </v-btn>

                  <v-btn icon>
                    <v-icon color="grey darken-2">forward</v-icon>{{feed.forwarded}}
                  </v-btn>

                  <v-btn icon>
                    <v-icon color="grey darken-2">queue_music</v-icon>
                  </v-btn>
                </v-card-actions>

                <v-divider></v-divider>
            </v-flex>

            <v-flex xs7 :key="index"></v-flex>
        </template>
    </v-layout>
</template>



<script>
  export default {
    data () {
      return {
        feeds: [
          {
            cover: require('../assets/images/feed1.jpg'),
            name: '',
            length: '',
            type: '',
            tag: '',
            liked: 12,
            forwarded: 11,
            shared: 13,
            listened: 17,
            upl_time: '12 hours ago',
            upl_avatar: 'https://cdn.vuetifyjs.com/images/lists/1.jpg',
            upl_name: 'John Leider'
          }
        ]
      }
    }
  }
</script>



<style>
    .btn-cover:hover {
        cursor: pointer;
    }
</style>
