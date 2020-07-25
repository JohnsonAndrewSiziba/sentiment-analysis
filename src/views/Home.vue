<template>
  <div class="home">
    <img alt="App logo" src="../assets/logo.png">
    <SentenceInput v-on:submit-sentence="submitSentence"/>
    <Results v-bind:results="results" v-show="results" />
  </div>
</template>

<script>
// @ is an alias to /src

import SentenceInput from "../components/SentenceInput";
import Results from "../components/Results";
import axios from "axios";
export default {
  name: 'Home',
  components: {
    Results,
    SentenceInput,
  },
  data(){
    return {
      results: null
    }
  },
  methods: {
    submitSentence(s){
      const url = "https://js-django-api.herokuapp.com"
      // const url = "http://127.0.0.1:8085"
      axios.post(`${url}/sentiment_analysis/`,
              {
                sentence: s.sentence,
              })
              // .then(data => console.log(data.data))
              .then(data => this.results = data.data)
              .catch(err => console.log(err))

      console.log(this.results)
    }
  }
}
</script>
