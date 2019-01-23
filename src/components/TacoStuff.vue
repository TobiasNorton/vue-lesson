<template>
  <div class="background">
    <p v-for="(data, index) in tacos" :key="index">I have a {{ data.taco }} taco.</p>
    <p v-if="tacos.length >= 4">You are wise.</p>
    <p else>I need more tacos.</p>
  </div>
</template>

<script>
export default {
  name: "Taco-Stuff",
  data() {
    return {
      tacos: [
        { taco: "carnitas" },
        { taco: "super awesome al pastor" },
        { taco: "weird" }
      ]
    };
  }
};
</script>

<style>
.background {
  background-color: hsl(185, 50%, 75%);
  padding: 3rem;
}
</style>