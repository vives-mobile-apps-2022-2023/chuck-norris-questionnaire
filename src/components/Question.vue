<script setup lang="ts">
import { ref } from 'vue';

const question = ref({
  text: 'What is a known fact of Chuck Norris ?',
  image: 'https://images.t-online.de/2021/06/88660848v2/368x0:1241x1241/fit-in/1800x0/chuck-norris-der-schauspieler-ist-fuenffacher-vater.jpg',
  options: [
    { text: 'Chuck Norris breathes air ... five times a day', correct: true },
    { text: 'When God said, "Let there be light!" Chuck said, "Say Please."', correct: true },
    { text: 'Chuck Norris does not sleep. He waits.', correct: true },
    { text: 'The chief export of Chuck Norris is pain.', correct: true },
  ]
})

</script>

<template>
  <v-row>
    <v-col cols="12" sm="8">

      <v-card color="black">
        <v-card-title>
          Question 1
        </v-card-title>
        <v-card-text>
          {{ question.text }}
        </v-card-text>
      </v-card>

      <v-sheet class="mt-4 hidden-sm-and-up">
        <v-img :src="question.image" />
      </v-sheet>

      <v-sheet class="pa-8">
        <v-row v-for="(option, i) in question.options" :key="`opt${i}`">
          <!-- Text center center the content -->
          <v-col cols="2" class="d-flex align-center text-center">
            HIT
          </v-col>
          <v-col cols="10">
            <p>{{ option.text }}</p>
          </v-col>
        </v-row>
      </v-sheet>

    </v-col>
    <v-col cols="12" sm="4" class="hidden-xs">
      <v-img :src="question.image" />
    </v-col>

  </v-row>

</template>