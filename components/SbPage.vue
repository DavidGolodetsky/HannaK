<template>
  <div v-editable="blok">
    <SbHero :blok="blok.body[0]" />
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
