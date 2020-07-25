<template>
  <div class="home">
    <img alt="App logo" src="../assets/logo.png">
    <SentenceInput />
    <Results />
  </div>
</template>

<script>
// @ is an alias to /src

import SentenceInput from "../components/SentenceInput";
import Results from "../components/Results";
export default {
  name: 'Home',
  components: {
    Results,
    SentenceInput
  }
}
</script>
