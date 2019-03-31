<template>
  <v-container>
    <v-layout
      text-xs-center
      wrap
    >
      <v-flex xs12>
        <v-img
          :src="require('../assets/logo.svg')"
          class="my-3"
          contain
          height="200"
        ></v-img>
      </v-flex>

      <v-flex mb-4>
        <h1 class="display-2 font-weight-bold mb-3">
          Welcome to ESL
        </h1>
        <p class="subheading font-weight-regular">
          We meet your software development needs
          
        </p>
      </v-flex>

      <v-flex
        mb-5
        xs12
      >
        <h2 class="headline font-weight-bold mb-3">What do we do?</h2>

        <!-- <v-flex xs12 sm6 offset-sm3>
        <v-card>
          <v-img
            src="https://cdn.vuetifyjs.com/images/cards/desert.jpg"
            aspect-ratio="2.75"
          ></v-img>
  
          <v-card-title primary-title>
            <div>
              <h3 class="headline mb-0">Kangaroo Valley Safari</h3>
              <div> {{ card_text }} </div>
            </div>
          </v-card-title>
  
          <v-card-actions>
            <v-btn flat color="orange">Share</v-btn>
            <v-btn flat color="orange">Explore</v-btn>
          </v-card-actions>
        </v-card>
      </v-flex> -->
      <!-- TODO: Make this tile better by adding title bar inside the card and contents to display nicely
      play around with differnt options -->
      <v-flex v-for="(next, i) in whatsNext" :key="i" sm12 mb-2>
        <v-layout justify-center>
          <v-card class="elevation-20" style="height:100%" width="300">
          <v-card-title primary-title>
            <h3 class="headline mb-0">{{ next.text }}</h3>
          </v-card-title>
          <v-card-text>
            {{next.description}}
          </v-card-text>
          </v-card>
        </v-layout>
      </v-flex>
        
      </v-flex>
    </v-layout>
  </v-container>
</template>

<script>
  export default {
    data: () => ({
      whatsNext: [
        {
          text: 'App Development',
          href: 'https://en.wikipedia.org/wiki/Mobile_app_development',
          description: 'We do web/i-phone/android application. We prefer to develop most of the features platform independent.'
        },
        {
          text: 'Artifical Intelligence',
          href: 'https://en.wikipedia.org/wiki/Artificial_intelligence',
          description: 'Since artificial intelligence is domain specific we work with clients to understand the problem and recommend hybrid approach to solve the problem'
        },
        {
          text: 'Image Processing',
          href: 'https://en.wikipedia.org/wiki/Digital_image_processing',
          description: 'We use raspberry pi and other inexpensive tools to prototype signal processing projects'
        }

      ]
    })
  }
</script>

<style>

</style>
