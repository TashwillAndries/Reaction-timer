<template>
  <p>Reation Time: {{ score }}m/s</p>
  <p class="rank">{{ rank }}</p>
</template>

<script>
export default {
  props: ["score"],
  data() {
    return {
      rank: null,
    };
  },
  mounted() {
    if (this.score < 350) {
      this.rank = "your girl must be happy fingers";
    } else if (this.score < 400) {
      this.rank = "Getting there";
    } else {
      this.rank = "You suck get good son";
    }
  },
};
</script>

<style>
.rank {
  font-size: 1.4rem;
  color: #0faf87;
  font-weight: bold;
}
</style>
