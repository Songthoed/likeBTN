<template>
  <div class="row">
    <div class="col-12">
      <button v-on:click="upfunction" class="btn btn-info">up</button>
      <button v-on:click="downfunction" class="btn btn-info">down</button>
      <p v-bind:style="{fontSize: fsize + 'px'}">HELLO</p>
    </div>
  </div>
</template>

<script>
export default {
  data: function () {
    return {
      fsize: 50,
    };
  },
  methods: {
    upfunction: function () {
      this.fsize += 10;
      console.log(this.fsize);
      this.$emit("cc", this.fsize);
    },
    downfunction: function () {
      this.fsize -= 10;
      console.log(this.fsize);
      this.$emit("cc", this.fsize);
    },
  },
};
</script>

<style>
</style>