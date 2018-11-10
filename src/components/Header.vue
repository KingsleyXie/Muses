<template>
  <v-toolbar color="white">

    <v-img
        :src="require('../assets/images/logo.jpg')"
        height="64px"
    ></v-img>

    <v-spacer></v-spacer>
    <v-text-field
        class="mx-3"
        flat
        single-line
        label="Search Muses"
        prepend-inner-icon="search"
    ></v-text-field>

    <v-spacer></v-spacer>
    <v-btn
      color="pink lighten-3"
      class="white--text"
      @click.native="loader = 'loading3'"
    >
      <v-icon left dark>cloud_upload</v-icon>
      Upload
    </v-btn>
    <v-btn
      color="pink lighten-3"
      class="white--text"
      @click.native="loader = 'loading3'"
    >
      <v-icon left dark>widgets</v-icon>
      Categories
    </v-btn>
    
    <v-spacer></v-spacer>

    <v-layout
    justify-center
  >
        <v-avatar>
            <img
            :src="require('../assets/images/avatar.png')"
            alt="Avatar"
            >
            nekogee
            <v-icon right color="black">expand_more</v-icon>
        </v-avatar>
    </v-layout>
  </v-toolbar>
</template>

<style>
.v-image__image--cover {
    background-size: auto;
}
</style>
