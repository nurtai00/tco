<script>
import json from '@/components/templates/News/json_data.json'
export default {
  data() {
    return {
      data: json
    }
  },
  computed: {
    id() {
      return this.$route.params.id
    },
    lang() {
      return this.$i18n.locale
    },
    news() {
      return this.data[this.id]
    },
    tags() {
      return [
        {
          text: this.$t('news.tags[0]'),
          value: '',
          selected: false,
          color: '#D92D20'
        },
        {
          text: this.$t('news.tags[1]'),
          value: '',
          selected: false,
          color: '#FFC000'
        },
        {
          text: this.$t('news.tags[2]'),
          value: '',
          selected: false,
          color: '#53389E'
        },
        {
          text: this.$t('news.tags[3]'),
          value: '',
          selected: false,
          color: '#D92D20'
        },
        {
          text: this.$t('news.tags[4]'),
          value: '',
          selected: false,
          color: '#00B0F0'
        },
        {
          text: this.$t('news.tags[5]'),
          value: '',
          selected: false,
          color: '#D92D20'
        }
      ]
    },
  },
}
</script>
<template>
  <div class="news container">
    <MoleculesBreadcrumbs class="mt40 mb40">
      <AtomsBreadOption to="/">
        {{ $t('news.breadcrumbs_1[0]') }}
      </AtomsBreadOption>
      <AtomsBreadOption to="/news">
        {{ $t('news.breadcrumbs_1[1]') }}
      </AtomsBreadOption>
    </MoleculesBreadcrumbs>
    <div class="content">
      <AtomsHeading type="h3" color="main" class="mb20">
        {{ news[lang].title }}
      </AtomsHeading>
      <AtomsTag
        :tag="{
          text: '#' + tags[news[lang].category].text,
          selected: true,
        }"
        class="tag"
      />
      <p class="content_date">{{ news[lang].date }}</p>
      <img :src="require(`@/assets/img/new/` + news[lang].img)" />
      <p class="content_text">
        {{ news[lang].body }}
      </p>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.news {
  width: 100%;
  padding-bottom: 100px;
}
.content {
  width: 896px;
  margin: 0 auto;
  @media only screen and (max-width: 1024px) {
    width: 100%;
    margin: 0px;
  }

  &_date {
    font-family: 'Roboto', sans-serif;
    font-weight: 400;
    font-size: 20px;
    line-height: 28px;
    color: #5e8698;
    margin: 40px 0 20px;
    @include tablet() {
      font-size: 14px;
      line-height: 18px;
      margin: 20px 0 12px 0;
    }
  }
  img {
    width: 100%;
    margin-bottom: 40px;
    @include tablet() {
      margin-bottom: 20px;
    }
  }
  &_text {
    font-family: 'Roboto', sans-serif;
    font-weight: 300;
    font-size: 20px;
    line-height: 28px;
    color: #30454e;
    @include tablet() {
      font-size: 14px;
      line-height: 18px;
    }
  }
}
.tag {
  margin: 0;
}
</style>
