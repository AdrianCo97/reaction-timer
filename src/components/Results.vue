<template>
  <p>My score: {{ score }}</p>
</template>

<script>
export default {
  props: ["score"],
  data() {
    return {
      result: 0,
    };
  },
};
</script>
