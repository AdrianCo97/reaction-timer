<template>
  <p>My score: {{ score }}</p>
  <p v-if="!slowReaction">Fast reaction</p>
  <p v-else>Slow reaction</p>
</template>

<script>
export default {
  props: ["score"],
  data() {
    return {
      slowReaction: false
    };
  },
  mounted(){
    this.determineReaction(this.score)
  },
  methods: {
    determineReaction(score){
        if(score > 500){
            console.log("higher")
            this.slowReaction = true;
        }
    }
  }
};
</script>
