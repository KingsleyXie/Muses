<template>
    <v-layout row wrap>
        <template  v-for="(feed, index) in feeds">
            <v-flex xs5 :key="index" class="my-3">
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

            <v-flex xs1 :key="index"></v-flex>

            <v-flex xs6 :key="index">
                <p class="title mt-5">{{feed.name}}</p>

                <p class="subheading">By <a href="#" class="author">{{feed.author}}</a></p>

                <v-chip color="pink lighten-1" text-color="white">
                    Duration: {{feed.length}}<v-icon right>album</v-icon>
                </v-chip>

                <v-spacer></v-spacer>

                <v-chip outline color="pink lighten-1">
                    <v-icon left>apps</v-icon>{{feed.type}}
                </v-chip>

                <v-spacer></v-spacer>

                <v-chip label color="pink lighten-1" text-color="white" class="mt-5">
                    <v-icon left>label</v-icon>{{feed.tag}}
                </v-chip>
            </v-flex>
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
            name: 'Electrik Playground 10/11/18 inc. Don Diablo Guest Mix',
            author: 'Andi Durrant',
            length: '15:23',
            type: 'Ambient',
            tag: 'Sounding',
            liked: 12,
            forwarded: 11,
            shared: 13,
            listened: 17,
            upl_time: '12 hours ago',
            upl_avatar: 'https://cdn.vuetifyjs.com/images/lists/2.jpg',
            upl_name: 'John Leider'
          },
          {
            cover: require('../assets/images/feed2.jpg'),
            name: 'POSH DJ Mikey B 11.6.18 *Explicit',
            author: 'POSH DJs',
            length: '01:25:13',
            type: 'Bass',
            tag: 'House',
            liked: 9,
            forwarded: 2,
            shared: 3,
            listened: 15,
            upl_time: '10 hours ago',
            upl_avatar: 'https://cdn.vuetifyjs.com/images/lists/5.jpg',
            upl_name: 'Sampj Decap'
          },
          {
            cover: require('../assets/images/feed3.jpg'),
            name: 'Swanky Tunes - SHOWLAND 225',
            author: 'SWANKY TUNES',
            length: '21:11',
            type: 'Dess',
            tag: 'Tunes',
            liked: 19,
            forwarded: 11,
            shared: 17,
            listened: 23,
            upl_time: '7 hours ago',
            upl_avatar: 'https://cdn.vuetifyjs.com/images/lists/4.jpg',
            upl_name: 'Don Lehit'
          },
          {
            cover: require('../assets/images/feed4.jpg'),
            name: 'Jack Phillips Presents Ready for the Weekend #139',
            author: 'Jack_Phillips',
            length: '15:21',
            type: 'Present',
            tag: 'Phillipos',
            liked: 2,
            forwarded: 1,
            shared: 1,
            listened: 7,
            upl_time: '9 hours ago',
            upl_avatar: 'https://cdn.vuetifyjs.com/images/lists/2.jpg',
            upl_name: 'Noki'
          },
          {
            cover: require('../assets/images/feed5.jpg'),
            name: 'ZEMIXX 678, HAUNTED HOUSE',
            author: 'Joachim Garraud',
            length: '01:00:23',
            type: 'EDM',
            tag: 'zemixx',
            liked: 5,
            forwarded: 2,
            shared: 2,
            listened: 9,
            upl_time: '15 hours ago',
            upl_avatar: 'https://cdn.vuetifyjs.com/images/lists/3.jpg',
            upl_name: 'Kanoka'
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
    .author {
        color: black;
    }
</style>
