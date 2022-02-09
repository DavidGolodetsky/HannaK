<template>
  <div>
    <img
      v-if="blok.image"
      class="image w-full mb-4 object-cover"
      :src="blok.image.filename"
    />
    <div v-editable="blok" class="hero pb-8 mb-6 font-bold text-center">
      <h3 class="title text-5xl">{{ blok.headline }}</h3>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    blok: {
      type: Object,
      required: true,
    },
  },
};
</script>

<style scoped>
.hero {
  position: relative;
  height: 600px;
}
.image {
  position: absolute;
  left: 0;
  top: 0;
  width: 100vw;
  z-index: 0;
  height: 600px;
}
.title {
  position: absolute;
  color: aliceblue;
  left: 100px;
  bottom: 100px;
}
</style>
