<template>
  <div class="impact">
    <div class="impact__wrapper container">
      <AtomsHeading class="impact__title" type="h3">
        {{ $t('suistainability.impactPopulation.title') }}
      </AtomsHeading>
      <div class="impact__content">
        <div class="impact__info">
          <p class="impact__info-description">
            {{ $t('suistainability.impactPopulation.description') }}
          </p>
          <div class="mt40">
            <AtomsPdfFile
              :text="$t('suistainability.impactPopulation.files.file1')"
              direction="row"
              :width="30"
              :height="40"
              :href="keyEnvironmentalIndicators"
            />
            <AtomsPdfFile
              class="mt20"
              :href="landScapingHref"
              :text="$t('suistainability.impactPopulation.files.file2')"
              direction="row"
              :width="30"
              :height="40"
            />
          </div>
        </div>
        <div class="impact__img">
          <img
            src="@/assets/img/sustainability/ecology/bg.png"
            alt="block6-1"
          />
        </div>
      </div>
    </div>
    <div class="container impact__cards">
      <PopupCardWithImg
        v-for="item of items"
        :key="item.id"
        :item="item"
        @click="openPopup"
      />
    </div>
  </div>
</template>
<script>
import PopupCardWithImg from 'molecules/Card/PopupCardWithImg'
export default {
  components: { PopupCardWithImg },
  data() {
    return {
      items: [
        {
          id: 1,
          title: this.$t('suistainability.impactPopulation.cards.card1'),
          imgSrc: 'block1-1.png',
          popupText: this.$t(
            'suistainability.impactPopulation.popupText.card1'
          ),
          type: 'gaz',
        },
        {
          id: 2,
          title: this.$t('suistainability.impactPopulation.cards.card2'),
          imgSrc: 'block1-2.png',
          popupText: this.$t(
            'suistainability.impactPopulation.popupText.card2'
          ),
          bgSrc: 'popup-2.png',
        },
        {
          id: 3,
          title: this.$t('suistainability.impactPopulation.cards.card3'),
          imgSrc: 'block1-3.png',
          popupText: this.$t(
            'suistainability.impactPopulation.popupText.card3'
          ),
          bgSrc: 'popup-3.png',
        },
        {
          id: 4,
          title: this.$t('suistainability.impactPopulation.cards.card4'),
          imgSrc: 'block1-4.png',
          popupText: this.$t(
            'suistainability.impactPopulation.popupText.card4'
          ),
          videoUrl: 'https://www.youtube.com/embed/PjxueFd3QWc',
        },
      ],
    }
  },
  computed: {
    keyEnvironmentalIndicators() {
      const mapOfFileLink = {
        kk: 'https://norsecdeltaprojects-my.sharepoint.com/personal/n_nudiyev_norsec_kz/_layouts/15/download.aspx?UniqueId=062a4a18%2D5429%2D4ea9%2Dbaa1%2Da0df4ba3d946',
        ru: 'https://norsecdeltaprojects-my.sharepoint.com/personal/n_nudiyev_norsec_kz/_layouts/15/download.aspx?UniqueId=1b498f48%2D94e5%2D408e%2D8cb7%2D3f7a43425bba',
        en: 'https://norsecdeltaprojects-my.sharepoint.com/personal/n_nudiyev_norsec_kz/_layouts/15/download.aspx?UniqueId=00bf1b5c%2D5e9a%2D4864%2D948c%2D99a17f6fa156',
      }
      return mapOfFileLink[this.$i18n.locale]
    },

    landScapingHref() {
      const mapOfFileLink = {
        kk: 'https://drive.google.com/file/d/1isVDfSVS7MB_KkDXGV0aIkdOGUJ8_r3b/view',
        ru: 'https://drive.google.com/file/d/1-fEfxsDS7326dTpMHyPexPabrF3L7awJ/view?usp=share_link',
        en: 'https://drive.google.com/file/d/1WJenbR2GFMgy8f95Ih2AnWYr_VmojzGN/view',
      }
      return mapOfFileLink[this.$i18n.locale]
    },
    gazUtilizationUrl() {
      const mapOfUrls = {
        kk: 'https://www.youtube.com/embed/EpDzU9V7J_Q',
        ru: 'https://www.youtube.com/embed/368HYzkPlOY',
        en: 'https://www.youtube.com/embed/9NvcN9A7GsA',
      }
      return mapOfUrls[this.$i18n.locale]
    },
  },
  methods: {
    openPopup(item) {
      const videoUrl =
        item?.type === 'gaz' ? this.gazUtilizationUrl : item.videoUrl
      this.$modal.add({
        title: 'Default',
        payload: {
          title: item.title,
          modal: 'Default',
          text: item.popupText,
          imgSrc: item?.bgSrc,
          videoUrl,
        },
      })
    },
  },
}
</script>
<style lang="scss" scoped>
.impact {
  margin-top: 40px;
  background-color: #f2f6f7;
  padding: 80px 0;
  &__title {
    text-align: center;
  }
  &__content {
    margin-top: 40px;
    display: flex;
  }
  &__info {
    display: flex;
    flex-direction: column;
    min-width: 50%;
    padding-right: 20px;
    gap: 15px;
    width: 50%;
  }
  &__img {
    width: 100%;
    display: flex;
    justify-content: center;
    align-items: center;
    overflow: hidden;
    max-height: 600px;
    img {
      flex-shrink: 0;
      min-width: 100%;
      min-height: 100%;
    }
  }
  @include tablet {
    &__title {
      text-align: center;
    }
    &__content {
      margin-top: 20px;
      flex-direction: column-reverse;
    }
    &__img {
      width: 100%;
      img {
        width: 100%;
        height: 100%;
        position: inherit;
        margin-bottom: 20px;
      }
    }
    &__info {
      width: 100%;
      padding-right: 0;
      margin: 0 auto;
      &-description {
        font-size: 16px;
        font-weight: 400;
      }
    }
  }
  &__cards {
    margin-top: 40px;
    display: grid;
    grid-template-columns: repeat(4, 25%);
    gap: 20px;
    @include tablet {
      grid-template-columns: repeat(2, 50%);
      //justify-content: space-between;
      gap: 5px;
      row-gap: 20px;
    }
    @include phone {
    }
  }
}
</style>
