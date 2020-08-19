<template>
  <div>
    <div class="row">
      <div class="col-4"></div>
      <div class="col-4">
        <div class="row">
          <div class="col-2"></div>
          <div class="col-2">
            <button v-on:click="counter += 1" class="btn btn-info">
              <i class="fa fa-thumbs-o-up" aria-hidden="true"></i>
            </button>
          </div>
          <div class="col-2">
            <button v-on:click="counter -= 10" class="btn btn-info">
              <i class="fa fa-thumbs-o-down" aria-hidden="true"></i>
            </button>
          </div>
          <div class="col-2">
            <button v-on:click="counter += 5" class="btn btn-info">
              <i class="fa fa-heart-o" aria-hidden="true"></i>
            </button>
          </div>
          <div class="col-2">
            <button v-on:click="counter = 0" class="btn btn-info">
              <i class="fa fa-refresh" aria-hidden="true"></i>
            </button>
          </div>
        </div>
      </div>
    </div>
    <div class="point">{{counter}}</div>
  </div>
</template>
<script>
export default {
  data: function () {
    return {
      counter: 0,
    };
  },
};
</script>

<style>
</style>