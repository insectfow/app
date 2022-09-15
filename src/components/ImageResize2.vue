<template>
  <div class="image-wrap">
    <div v-if="!imageUrl">
      <label for="imageInput2">이미지</label>
    </div>
    <figure class="image" v-else>
      <img :src="imageUrl" alt="2" />
      <a :href="imageUrl" download>다운로드</a>
    </figure>
    <input
      class="image-input"
      id="imageInput2"
      type="file"
      accept="image/*"
      @change="imageUpload"
    />
  </div>
</template>

<script>
export default {
  data() {
    return {
      imageUrl: null,
      baseSize: 524000,
      compSize: 52400,
    };
  },
  methods: {
    imageUpload(e) {
      const file = e.target.files[0];
      console.log(file.size <= this.baseSize);
      if (file.size <= this.baseSize) return file;
      const ratio = Math.ceil(Math.sqrt((file.size / this.compSize) * 2));
      const fr = new FileReader();
      fr.onload = (base64) => {
        const image = new Image();
        image.src = base64.target.result;
        image.onload = (e) => {
          const $canvas = document.createElement(`canvas`);
          let width = image.width / ratio;
          let height = image.height / ratio;
          $canvas.width = width;
          $canvas.height = height;
          const ctx = $canvas.getContext(`2d`);
          ctx.drawImage(e.target, 0, 0, width, height);
          this.imageUrl = $canvas.toDataURL(`image/jpeg`, 1);
        };
      };
      fr.readAsDataURL(file);
    },
  },
};
</script>
<style lang="scss" scoped>
.image-wrap {
  box-shadow: 0 0 5px rgba(0, 0, 0, 0.2);
  .image-input {
    display: none;
  }
  .image {
    display: flex;
    width: 200px;
    height: 200px;
    > img {
      width: 100%;
    }
  }
}
</style>
