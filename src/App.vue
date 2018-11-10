<template>
  <v-app>
    <v-content>
      <Header></Header>

      <v-layout row wrap class="mt-3">
        <v-flex xs2></v-flex>

        <v-flex xs6>
          <Feed></Feed>
        </v-flex>

        <v-flex xs2>
          <SuggestPeople></SuggestPeople>
          <About></About>
        </v-flex>

        <v-flex xs2></v-flex>
      </v-layout>

    </v-content>
  </v-app>
</template>

<script>
import Header from './components/Header'
import Feed from './components/Feed'
import SuggestPeople from './components/SuggestPeople'
import About from './components/About'

export default {
  name: 'App',
  components: {
    Header,
    Feed,
    SuggestPeople,
    About
  },
  data () {
    return {}
  }
}
</script>
