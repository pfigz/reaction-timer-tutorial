<template>
  <div class="block" v-if="showBlock">Click Me</div>
</template>

<script>
export default {
  props: ["delay"],
  data() {
    return {
      showBlock: false,
    };
  },
  // Fires when component is mounted to the DOM
  mounted() {
    console.log("component mounted");
    setTimeout(() => {
      this.showBlock = true;
      console.log(this.delay);
    }, this.delay);
  },
  // Fires when component data is updated
  updated() {
    console.log("component updated");
  },
  // Fires when component is unmounte (removed) from DOM
  unmounted() {
    console.log("unmounted");
  },
};
</script>

<style scoped>
.block {
  width: 400px;
  border-radius: 20px;
  background: #0faf87;
  color: white;
  text-align: center;
  padding: 100px 0;
  margin: 40px auto;
}
</style>
