<template>
  <div class="blur-image-container">
    <img
      :src="src"
      :alt="alt"
      :class="['blur-image', loaded ? 'loaded' : '']"
      :width="width"
      :height="height"
      :loading="loading"
      @load="onLoaded"
      ref="imageRef"
    />
  </div>
</template>

<script>
export default {
  name: "BlurImage",
  props: {
    src: {
      type: String,
      required: true,
    },
    alt: {
      type: String,
      required: true,
    },
    width: {
      type: [Number, String],
      default: null,
    },
    height: {
      type: [Number, String],
      default: null,
    },
    loading: {
      type: String,
      default: "lazy",
      validator: (value) => ["lazy", "eager"].includes(value),
    },
  },
  data() {
    return {
      loaded: false,
    };
  },
  mounted() {
    // Check if image is already cached
    if (this.$refs.imageRef && this.$refs.imageRef.complete) {
      this.loaded = true;
    }
  },
  methods: {
    onLoaded() {
      this.loaded = true;
    },
  },
};
</script>

<style scoped>
.blur-image-container {
  overflow: hidden;
  width: 100%;
  height: 100%;
  position: relative;
}

.blur-image {
  filter: blur(15px);
  transform: scale(1.05);
  transition: filter 0.5s ease, transform 0.5s ease;
  width: 100%;
  height: 100%;
}

.blur-image.loaded {
  filter: blur(0);
  transform: scale(1);
}
</style>
