<template>
  <div class="p_card">
    <a :href="link" target="_blank">
      <img loading="lazy" :src="img" alt="publication_card" />
      <div>
        <img
          loading="lazy"
          src="@/assets/icons/pdf.png"
          alt="pdf"
          width="21"
          height="28"
        />
        <p>{{ text }}</p>
      </div>
    </a>
  </div>
</template>

<script>
export default {
  props: {
    img: {
      type: String,
      required: true,
    },
    text: {
      type: String,
      default: '',
    },
    link: {
      type: String,
      default: '',
    },
  },
}
</script>

<style scoped lang="scss">
.p_card {
  img {
    width: 100%;
  }
  div {
    display: grid;
    grid-template-columns: 21px 1fr;
    margin-top: 12px;
    p {
      font-family: 'Roboto', sans-serif;
      padding-left: 12px;
      font-weight: 500;
      font-size: 18px;
      line-height: 22px;
      color: #30454e;
      @media (orientation: portrait) {
        font-size: 14px;
        line-height: 18px;
      }
    }
  }
}
</style>
