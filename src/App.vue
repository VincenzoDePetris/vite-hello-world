<script>
export default {
  data() {
    return {
      title: "Hello World",
      image: "./assets/img/dog.jpg",
    };
  },
  methods: {
    buildImagePath(imageName) {
      const imageUrl = new URL(imageName, import.meta.url);
      console.log(imageUrl);
      return imageUrl.href;
    },
  },
};
</script>

<template>
  <h1>{{ title }}</h1>
  <div><img :src="buildImagePath(image)" alt="" /></div>
</template>

<style></style>
