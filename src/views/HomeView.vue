<template>
  <div class="home">
    <!-- {{ tweets }} -->
    <TweetVue 
      v-for="tweet in tweets" 
      :key="tweet._id" 
      :tweet="tweet" />
  </div>
</template>

<script>
import { ref } from 'vue';
import TweetVue from '../components/TweetVue';
import vweets from '../vweets';

export default {
  components: {
    TweetVue,
  },
  setup () {
    const tweets = ref(vweets);

    return {
      tweets,
      TweetVue
    }
  }
}
</script>