<script>
export default {
  computed: {
    fileLink() {
      const mapOfFileLinkUrl = {
        ru: 'https://norsecdeltaprojects-my.sharepoint.com/personal/n_nudiyev_norsec_kz/Documents/%D0%A0%D0%B0%D0%B1%D0%BE%D1%87%D0%B8%D0%B9%20%D1%81%D1%82%D0%BE%D0%BB/TCOntent/Main%20page/2021-%D0%BE%D1%82%D1%87%D0%B5%D1%82-%D0%BE-%D0%BA%D0%BE%D1%80%D0%BF%D0%BE%D1%80%D0%B0%D1%82%D0%B8%D0%B2%D0%BD%D0%BE%D0%B9-%D0%BE%D1%82%D0%B2%D0%B5%D1%82%D1%81%D1%82%D0%B2%D0%B5%D0%BD%D0%BD%D0%BE%D1%81%D1%82%D0%B8.pdf?CT=1670996186909&OR=ItemsView',
        kk: 'https://norsecdeltaprojects-my.sharepoint.com/personal/n_nudiyev_norsec_kz/Documents/%D0%A0%D0%B0%D0%B1%D0%BE%D1%87%D0%B8%D0%B9%20%D1%81%D1%82%D0%BE%D0%BB/TCOntent/Main%20page/2021-%D0%BA%D0%BE%D1%80%D0%BF%D0%BE%D1%80%D0%B0%D1%82%D0%B8%D0%B2%D1%82%D1%96%D0%BA-%D0%B6%D0%B0%D1%83%D0%B0%D0%BF%D0%BA%D0%B5%D1%80%D1%88%D1%96%D0%BB%D1%96%D0%BA-%D1%82%D1%83%D1%80%D0%B0%D0%BB%D1%8B-%D0%B5%D1%81%D0%B5%D0%BF.pdf?CT=1670996212309&OR=ItemsView',
        en: 'https://norsecdeltaprojects-my.sharepoint.com/personal/n_nudiyev_norsec_kz/Documents/%D0%A0%D0%B0%D0%B1%D0%BE%D1%87%D0%B8%D0%B9%20%D1%81%D1%82%D0%BE%D0%BB/TCOntent/Main%20page/2021-corporate-responsibility-report.pdf?CT=1670996277625&OR=ItemsView',
      }
      return mapOfFileLinkUrl[this.$i18n.locale]
    },
  },
}
</script>

<template>
  <div class="organismsSectionMainBlock3">
    <section style="padding: 80px 0 50px">
      <div class="container">
        <div class="tco__numbers">
          <div class="lines">
            <div class="section__title">
              <AtomsTitle class="atoms_title mb20" small>
                {{ $t('home.block_3.title') }}
              </AtomsTitle>
              <AtomsTitle class="atoms_title mb20 mobile" small>
                {{ $t('home.block_3.title_mobile_1') }}
              </AtomsTitle>
              <a :href="localePath('/#/about')" class="mb20">{{
                $t('home.block_3.link')
              }}</a>
            </div>
            <div class="line">
              <div>
                <span> {{ $t('home.block_3.items[0].title') }} </span>
                <p>{{ $t('home.block_3.items[0].text') }}</p>
              </div>
              <img src="@/assets/img/document-2.png" alt="" />
            </div>
            <div class="line">
              <div>
                <span> {{ $t('home.block_3.items[1].title') }} </span>
                <p>{{ $t('home.block_3.items[1].text') }}</p>
              </div>
              <img src="@/assets/img/barrels-2.png" alt="" />
            </div>
            <div class="line">
              <div>
                <span>{{ $t('home.block_3.items[2].title') }}</span>
                <p>{{ $t('home.block_3.items[2].text') }}</p>
              </div>
              <img src="@/assets/img/oil-pump-2.png" alt="" />
            </div>
          </div>
          <div class="card">
            <img src="@/assets/img/Rectangle 27.png" class="card__image" />
            <p>
              {{ $t('home.block_3.right.text') }}
            </p>
            <a
              :href="localePath('/#/projects')"
              style="font-family: Roboto, sans-serif"
            >
              {{ $t('home.block_3.right.link_1') }}
            </a>
            <a
              class="file"
              style="font-family: Roboto, sans-serif"
              :href="fileLink"
              target="_blank"
              rel="noopener noreferrer"
            >
              <img width="30" height="40" src="@/assets/img/pdf.png" />
              {{ $t('home.block_3.right.link_2') }}
            </a>
          </div>
        </div>
      </div>
    </section>
  </div>
</template>

<style scoped lang="scss">
%card-text-style {
  font-size: 18px;
  line-height: 20px;
  @media (max-width: 730px) {
    font-size: 16px;
    line-height: 20px;
  }
}
.tco {
  &__numbers {
    display: flex;
    justify-content: space-between;
    gap: 36px;
    @media (max-width: 730px) {
      flex-direction: column;
    }
    .card {
      display: flex;
      flex-direction: column;
      width: 40%;
      row-gap: 12px;
      @media (max-width: 730px) {
        width: 100%;
      }
      &__image {
        aspect-ratio: 1.9/1;
        object-fit: cover;
        flex: 1;
      }
      p {
        @extend %card-text-style;
        font-weight: 500;
      }
      .mobile {
        display: none;
      }
      a {
        @extend %card-text-style;
        display: flex;
        gap: 12px;
        text-decoration-line: underline;
        color: #00b0f0 !important;
        img {
          width: 30px;
        }
      }
      a:last-child {
        margin-top: 15px;
        color: #30454e !important;
      }
    }
    .lines {
      display: flex;
      flex-direction: column;
      gap: 20px;
      width: 60%;
      @media (max-width: 730px) {
        width: 100%;
      }
      .line {
        width: 100%;
        display: flex;
        justify-content: space-between;
        align-items: center;
        padding: 15px;
        background: #f2f6f7;
        border-radius: 4px;
        div {
          display: flex;
          flex-direction: column;
          row-gap: 12px;
          span {
            font-family: 'Montserrat';
            font-style: normal;
            font-weight: 700;
            font-size: 28px;
            line-height: 32px;
            color: #015467;
          }
          p {
            font-family: 'Roboto';
            font-style: normal;
            font-weight: 300;
            font-size: 16px;
            line-height: 20px;
            color: #30454e;
          }
        }
      }
    }
  }
}
.organismsSectionMainBlock3 {
  .card {
    .file {
      display: flex !important;
      background: rgba(1, 84, 103, 0.15);
      padding: 16px;
      font-family: 'Montserrat', sans-serif !important;
      color: #015467 !important;
      text-decoration: none;
      align-items: center;
      margin-top: 0 !important;
    }
  }
  @media (orientation: portrait) {
    .tco__numbers {
      gap: 0px;
      grid-gap: 0px;
    }
    .lines > * {
      display: none !important;
    }
    .lines .section__title {
      display: flex !important;
      a,
      .atoms_title {
        display: none !important;
      }
      .mobile {
        display: flex !important;
        margin-bottom: 0px !important;
      }
    }
    .card > * {
      display: none !important;
    }
    .card .file {
      font-weight: 700;
      font-size: 20px;
      line-height: 26px;
      img {
        width: 26vw;
        height: 14vh;
      }
    }
  }
  .mobile {
    display: none;
  }
}
</style>
