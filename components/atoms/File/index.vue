<template>
  <div class="file">
    <div class="file__image">
      <img :src="`${require(`@/assets/img/${icon}.png`)}`" alt="file format" />
    </div>
    <a
      :href="file"
      class="file__name"
      target="_blank"
      rel="noopener noreferrer"
    >
      {{ text }}
    </a>
  </div>
</template>

<script>
export default {
  name: 'File',
  props: {
    file: {
      type: String,
      required: true,
    },
    text: {
      type: String,
      default: '',
    },
    icon: {
      type: String,
      required: true,
    },
  },
}
</script>

<style lang="scss" scoped>
.file {
  display: flex;
  align-items: center;
  margin-bottom: 20px;

  &__image {
    min-width: 30px;
    width: 30px;
    height: 40px;
    margin-right: 8px;

    img {
      width: 100%;
      height: 100%;
    }
  }

  &__name {
    font-size: 20px;
    line-height: 28px;
    color: #30454e;
    text-decoration: underline;

    @include phone {
      font-size: 14px;
      line-height: 18px;
      color: #00b0f0;
    }
  }
}
</style>
