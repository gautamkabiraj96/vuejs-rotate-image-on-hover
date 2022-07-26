<template>
  <div id="app">
    <div>
      <img
        :src="$options.imgUrl"
        :class="{
          'img-default': true,
          'img-rotated': imageRotated,
        }"
        @mouseover="imageRotated = true"
        @mouseout="imageRotated = false"
      />
    </div>
    <div class="np-credits">wwww.nightprogrammer.com</div>
  </div>
</template>

<script>
export default {
  name: "ImageRotated",
  created() {
    this.$options.imgUrl =
      "https://media-cldnry.s-nbcnews.com/image/upload/t_fit-1240w,f_auto,q_auto:best/rockcms/2022-01/220131-European-larch-trees-and-spruces-ew-512p-ec27db.jpg";
  },
  data() {
    return {
      imageRotated: false,
    };
  },
};
</script>

<style>
.img-default {
  height: 300px;
  transition: all 0.2s;
}

.img-rotated {
  height: 300px;
  transform: rotate(-10deg);
  transition: all 0.2s;
}

.np-credits {
  font-size: 12px;
  margin-bottom: 12px;
  color: #4b4b4b;
}
</style>