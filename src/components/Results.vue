<template>
  <p>Reaction time is {{ score }}</p>
  <h1 class="rank">{{ rank }}</h1>
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
      this.rank = "Gunslinger Reflex";
    } else if (this.score < 600) {
      this.rank = "Not bad , Try again :D";
    } else {
      this.rank = "Seriously Cowboy , Gotta work on your reflex ! :(";
    }
  },
};
</script>

<style>
.rank {
  color: darkcyan;
  font-weight: 500;
  font-size: 1.6rem;
}
</style>
