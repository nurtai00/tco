<template>
  <div class="p_block">
    <div class="p_block_title">
      <AtomsTitle small> {{ $t('news.pub') }} </AtomsTitle>
      <nuxt-link :to="localePath('/news/publications')">
        {{ $t('news.pub_all') }}
      </nuxt-link>
    </div>
    <div class="p_block_list">
      <MoleculesCardPublicationCard
        v-for="(item, index) in publications_list[$i18n.locale].slice(0, 4)"
        :key="item.link"
        :text="item.name"
        :link="item.link"
        :img="require(`@/assets/img/pub${index + 1}.png`)"
      />
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      publications_list: {
        ru: [
          {
            name: '2017-csrr-rus.pdf',
            link: 'https://norsecdeltaprojects-my.sharepoint.com/personal/n_nudiyev_norsec_kz/_layouts/15/onedrive.aspx?ga=1&id=%2Fpersonal%2Fn%5Fnudiyev%5Fnorsec%5Fkz%2FDocuments%2F%D0%A0%D0%B0%D0%B1%D0%BE%D1%87%D0%B8%D0%B9%20%D1%81%D1%82%D0%BE%D0%BB%2FTCOntent%2FAll%20Publications%20page%2FRU%2F2017%2Dcsrr%2Drus%2Epdf&parent=%2Fpersonal%2Fn%5Fnudiyev%5Fnorsec%5Fkz%2FDocuments%2F%D0%A0%D0%B0%D0%B1%D0%BE%D1%87%D0%B8%D0%B9%20%D1%81%D1%82%D0%BE%D0%BB%2FTCOntent%2FAll%20Publications%20page%2FRU',
          },
          {
            name: '2017-year-in-review_erk_final (1).pdf',
            link: 'https://norsecdeltaprojects-my.sharepoint.com/personal/n_nudiyev_norsec_kz/_layouts/15/onedrive.aspx?ga=1&id=%2Fpersonal%2Fn%5Fnudiyev%5Fnorsec%5Fkz%2FDocuments%2F%D0%A0%D0%B0%D0%B1%D0%BE%D1%87%D0%B8%D0%B9%20%D1%81%D1%82%D0%BE%D0%BB%2FTCOntent%2FAll%20Publications%20page%2FRU%2F2017%2Dyear%2Din%2Dreview%5Ferk%5Ffinal%20%281%29%2Epdf&parent=%2Fpersonal%2Fn%5Fnudiyev%5Fnorsec%5Fkz%2FDocuments%2F%D0%A0%D0%B0%D0%B1%D0%BE%D1%87%D0%B8%D0%B9%20%D1%81%D1%82%D0%BE%D0%BB%2FTCOntent%2FAll%20Publications%20page%2FRU',
          },
          {
            name: '2018-corporate-responsibility-report (2).pdf',
            link: 'https://norsecdeltaprojects-my.sharepoint.com/personal/n_nudiyev_norsec_kz/_layouts/15/onedrive.aspx?ga=1&id=%2Fpersonal%2Fn%5Fnudiyev%5Fnorsec%5Fkz%2FDocuments%2F%D0%A0%D0%B0%D0%B1%D0%BE%D1%87%D0%B8%D0%B9%20%D1%81%D1%82%D0%BE%D0%BB%2FTCOntent%2FAll%20Publications%20page%2FRU%2F2018%2Dcorporate%2Dresponsibility%2Dreport%20%282%29%2Epdf&parent=%2Fpersonal%2Fn%5Fnudiyev%5Fnorsec%5Fkz%2FDocuments%2F%D0%A0%D0%B0%D0%B1%D0%BE%D1%87%D0%B8%D0%B9%20%D1%81%D1%82%D0%BE%D0%BB%2FTCOntent%2FAll%20Publications%20page%2FRU',
          },
          {
            name: '2021-??????????-??-??????????????????????????-??????????????????????????????.pdf',
            link: 'https://norsecdeltaprojects-my.sharepoint.com/personal/n_nudiyev_norsec_kz/_layouts/15/onedrive.aspx?ga=1&id=%2Fpersonal%2Fn%5Fnudiyev%5Fnorsec%5Fkz%2FDocuments%2F%D0%A0%D0%B0%D0%B1%D0%BE%D1%87%D0%B8%D0%B9%20%D1%81%D1%82%D0%BE%D0%BB%2FTCOntent%2FAll%20Publications%20page%2FRU%2F2021%2D%D0%BE%D1%82%D1%87%D0%B5%D1%82%2D%D0%BE%2D%D0%BA%D0%BE%D1%80%D0%BF%D0%BE%D1%80%D0%B0%D1%82%D0%B8%D0%B2%D0%BD%D0%BE%D0%B9%2D%D0%BE%D1%82%D0%B2%D0%B5%D1%82%D1%81%D1%82%D0%B2%D0%B5%D0%BD%D0%BD%D0%BE%D1%81%D1%82%D0%B8%2Epdf&parent=%2Fpersonal%2Fn%5Fnudiyev%5Fnorsec%5Fkz%2FDocuments%2F%D0%A0%D0%B0%D0%B1%D0%BE%D1%87%D0%B8%D0%B9%20%D1%81%D1%82%D0%BE%D0%BB%2FTCOntent%2FAll%20Publications%20page%2FRU',
          },
          {
            name: 'feedback-management-process-flyer (2).pdf',
            link: 'https://norsecdeltaprojects-my.sharepoint.com/personal/n_nudiyev_norsec_kz/_layouts/15/onedrive.aspx?ga=1&id=%2Fpersonal%2Fn%5Fnudiyev%5Fnorsec%5Fkz%2FDocuments%2F%D0%A0%D0%B0%D0%B1%D0%BE%D1%87%D0%B8%D0%B9%20%D1%81%D1%82%D0%BE%D0%BB%2FTCOntent%2FAll%20Publications%20page%2FRU%2Ffeedback%2Dmanagement%2Dprocess%2Dflyer%20%282%29%2Epdf&parent=%2Fpersonal%2Fn%5Fnudiyev%5Fnorsec%5Fkz%2FDocuments%2F%D0%A0%D0%B0%D0%B1%D0%BE%D1%87%D0%B8%D0%B9%20%D1%81%D1%82%D0%BE%D0%BB%2FTCOntent%2FAll%20Publications%20page%2FRU',
          },
          {
            name: 'iv_kazcont_rus_2017.pdf',
            link: 'https://norsecdeltaprojects-my.sharepoint.com/personal/n_nudiyev_norsec_kz/_layouts/15/onedrive.aspx?ga=1&id=%2Fpersonal%2Fn%5Fnudiyev%5Fnorsec%5Fkz%2FDocuments%2F%D0%A0%D0%B0%D0%B1%D0%BE%D1%87%D0%B8%D0%B9%20%D1%81%D1%82%D0%BE%D0%BB%2FTCOntent%2FAll%20Publications%20page%2FRU%2Fiv%5Fkazcont%5Frus%5F2017%2Epdf&parent=%2Fpersonal%2Fn%5Fnudiyev%5Fnorsec%5Fkz%2FDocuments%2F%D0%A0%D0%B0%D0%B1%D0%BE%D1%87%D0%B8%D0%B9%20%D1%81%D1%82%D0%BE%D0%BB%2FTCOntent%2FAll%20Publications%20page%2FRU',
          },
          {
            name: 'tco_2015_2016_corporate-responsibility-report_r.pdf',
            link: 'https://norsecdeltaprojects-my.sharepoint.com/personal/n_nudiyev_norsec_kz/_layouts/15/onedrive.aspx?ga=1&id=%2Fpersonal%2Fn%5Fnudiyev%5Fnorsec%5Fkz%2FDocuments%2F%D0%A0%D0%B0%D0%B1%D0%BE%D1%87%D0%B8%D0%B9%20%D1%81%D1%82%D0%BE%D0%BB%2FTCOntent%2FAll%20Publications%20page%2FRU%2Ftco%5F2015%5F2016%5Fcorporate%2Dresponsibility%2Dreport%5Fr%2Epdf&parent=%2Fpersonal%2Fn%5Fnudiyev%5Fnorsec%5Fkz%2FDocuments%2F%D0%A0%D0%B0%D0%B1%D0%BE%D1%87%D0%B8%D0%B9%20%D1%81%D1%82%D0%BE%D0%BB%2FTCOntent%2FAll%20Publications%20page%2FRU',
          },
          {
            name: '??????????????-???????????? (1).pdf',
            link: 'https://norsecdeltaprojects-my.sharepoint.com/personal/n_nudiyev_norsec_kz/_layouts/15/onedrive.aspx?ga=1&id=%2Fpersonal%2Fn%5Fnudiyev%5Fnorsec%5Fkz%2FDocuments%2F%D0%A0%D0%B0%D0%B1%D0%BE%D1%87%D0%B8%D0%B9%20%D1%81%D1%82%D0%BE%D0%BB%2FTCOntent%2FAll%20Publications%20page%2FRU%2F%D0%B1%D1%80%D0%BE%D1%88%D1%8E%D1%80%D0%B0%2D%D0%B8%D0%B3%D0%B8%D0%BB%D0%B8%D0%BA%20%281%29%2Epdf&parent=%2Fpersonal%2Fn%5Fnudiyev%5Fnorsec%5Fkz%2FDocuments%2F%D0%A0%D0%B0%D0%B1%D0%BE%D1%87%D0%B8%D0%B9%20%D1%81%D1%82%D0%BE%D0%BB%2FTCOntent%2FAll%20Publications%20page%2FRU',
          },
          {
            name: '??????????-2018-????????.pdf',
            link: 'https://norsecdeltaprojects-my.sharepoint.com/personal/n_nudiyev_norsec_kz/_layouts/15/onedrive.aspx?ga=1&id=%2Fpersonal%2Fn%5Fnudiyev%5Fnorsec%5Fkz%2FDocuments%2F%D0%A0%D0%B0%D0%B1%D0%BE%D1%87%D0%B8%D0%B9%20%D1%81%D1%82%D0%BE%D0%BB%2FTCOntent%2FAll%20Publications%20page%2FRU%2F%D0%B8%D1%82%D0%BE%D0%B3%D0%B8%2D2018%2D%D0%B3%D0%BE%D0%B4%D0%B0%2Epdf&parent=%2Fpersonal%2Fn%5Fnudiyev%5Fnorsec%5Fkz%2FDocuments%2F%D0%A0%D0%B0%D0%B1%D0%BE%D1%87%D0%B8%D0%B9%20%D1%81%D1%82%D0%BE%D0%BB%2FTCOntent%2FAll%20Publications%20page%2FRU',
          },
          {
            name: '??????????-2019-????????.pdf',
            link: 'https://norsecdeltaprojects-my.sharepoint.com/personal/n_nudiyev_norsec_kz/_layouts/15/onedrive.aspx?ga=1&id=%2Fpersonal%2Fn%5Fnudiyev%5Fnorsec%5Fkz%2FDocuments%2F%D0%A0%D0%B0%D0%B1%D0%BE%D1%87%D0%B8%D0%B9%20%D1%81%D1%82%D0%BE%D0%BB%2FTCOntent%2FAll%20Publications%20page%2FRU%2F%D0%B8%D1%82%D0%BE%D0%B3%D0%B8%2D2019%2D%D0%B3%D0%BE%D0%B4%D0%B0%2Epdf&parent=%2Fpersonal%2Fn%5Fnudiyev%5Fnorsec%5Fkz%2FDocuments%2F%D0%A0%D0%B0%D0%B1%D0%BE%D1%87%D0%B8%D0%B9%20%D1%81%D1%82%D0%BE%D0%BB%2FTCOntent%2FAll%20Publications%20page%2FRU',
          },
          {
            name: '????????????????-??????????????????????????-????????????????????-????-2021-??????.pdf',
            link: 'https://norsecdeltaprojects-my.sharepoint.com/personal/n_nudiyev_norsec_kz/_layouts/15/onedrive.aspx?ga=1&id=%2Fpersonal%2Fn%5Fnudiyev%5Fnorsec%5Fkz%2FDocuments%2F%D0%A0%D0%B0%D0%B1%D0%BE%D1%87%D0%B8%D0%B9%20%D1%81%D1%82%D0%BE%D0%BB%2FTCOntent%2FAll%20Publications%20page%2FRU%2F%D0%BE%D1%81%D0%BD%D0%BE%D0%B2%D0%BD%D1%8B%D0%B5%2D%D1%8D%D0%BA%D0%BE%D0%BB%D0%BE%D0%B3%D0%B8%D1%87%D0%B5%D1%81%D0%BA%D0%B8%D0%B5%2D%D0%BF%D0%BE%D0%BA%D0%B0%D0%B7%D0%B0%D1%82%D0%B5%D0%BB%D0%B8%2D%D0%B7%D0%B0%2D2021%2D%D0%B3%D0%BE%D0%B4%2Epdf&parent=%2Fpersonal%2Fn%5Fnudiyev%5Fnorsec%5Fkz%2FDocuments%2F%D0%A0%D0%B0%D0%B1%D0%BE%D1%87%D0%B8%D0%B9%20%D1%81%D1%82%D0%BE%D0%BB%2FTCOntent%2FAll%20Publications%20page%2FRU',
          },
          {
            name: '??????????-??-??????????????????????????-??????????????????????????????-????-2019-20-????.pdf',
            link: 'https://norsecdeltaprojects-my.sharepoint.com/personal/n_nudiyev_norsec_kz/_layouts/15/onedrive.aspx?ga=1&id=%2Fpersonal%2Fn%5Fnudiyev%5Fnorsec%5Fkz%2FDocuments%2F%D0%A0%D0%B0%D0%B1%D0%BE%D1%87%D0%B8%D0%B9%20%D1%81%D1%82%D0%BE%D0%BB%2FTCOntent%2FAll%20Publications%20page%2FRU%2F%D0%BE%D1%82%D1%87%D0%B5%D1%82%2D%D0%BE%2D%D0%BA%D0%BE%D1%80%D0%BF%D0%BE%D1%80%D0%B0%D1%82%D0%B8%D0%B2%D0%BD%D0%BE%D0%B9%2D%D0%BE%D1%82%D0%B2%D0%B5%D1%82%D1%81%D1%82%D0%B2%D0%B5%D0%BD%D0%BD%D0%BE%D1%81%D1%82%D0%B8%2D%D0%B7%D0%B0%2D2019%2D20%2D%D0%B3%D0%B3%2Epdf&parent=%2Fpersonal%2Fn%5Fnudiyev%5Fnorsec%5Fkz%2FDocuments%2F%D0%A0%D0%B0%D0%B1%D0%BE%D1%87%D0%B8%D0%B9%20%D1%81%D1%82%D0%BE%D0%BB%2FTCOntent%2FAll%20Publications%20page%2FRU',
          },
        ],
        en: [
          {
            name: '2017-year-in-review_erk_final.pdf',
            link: 'https://norsecdeltaprojects-my.sharepoint.com/personal/n_nudiyev_norsec_kz/_layouts/15/onedrive.aspx?ga=1&id=%2Fpersonal%2Fn%5Fnudiyev%5Fnorsec%5Fkz%2FDocuments%2F%D0%A0%D0%B0%D0%B1%D0%BE%D1%87%D0%B8%D0%B9%20%D1%81%D1%82%D0%BE%D0%BB%2FTCOntent%2FAll%20Publications%20page%2FEN%2F2017%2Dyear%2Din%2Dreview%5Ferk%5Ffinal%2Epdf&parent=%2Fpersonal%2Fn%5Fnudiyev%5Fnorsec%5Fkz%2FDocuments%2F%D0%A0%D0%B0%D0%B1%D0%BE%D1%87%D0%B8%D0%B9%20%D1%81%D1%82%D0%BE%D0%BB%2FTCOntent%2FAll%20Publications%20page%2FEN',
          },
          {
            name: '2018-corporate-responsibility-report.pdf',
            link: 'https://norsecdeltaprojects-my.sharepoint.com/personal/n_nudiyev_norsec_kz/_layouts/15/onedrive.aspx?ga=1&id=%2Fpersonal%2Fn%5Fnudiyev%5Fnorsec%5Fkz%2FDocuments%2F%D0%A0%D0%B0%D0%B1%D0%BE%D1%87%D0%B8%D0%B9%20%D1%81%D1%82%D0%BE%D0%BB%2FTCOntent%2FAll%20Publications%20page%2FEN%2F2018%2Dcorporate%2Dresponsibility%2Dreport%2Epdf&parent=%2Fpersonal%2Fn%5Fnudiyev%5Fnorsec%5Fkz%2FDocuments%2F%D0%A0%D0%B0%D0%B1%D0%BE%D1%87%D0%B8%D0%B9%20%D1%81%D1%82%D0%BE%D0%BB%2FTCOntent%2FAll%20Publications%20page%2FEN',
          },
          {
            name: '2018-year-in-review.pdf',
            link: 'https://norsecdeltaprojects-my.sharepoint.com/personal/n_nudiyev_norsec_kz/_layouts/15/onedrive.aspx?ga=1&id=%2Fpersonal%2Fn%5Fnudiyev%5Fnorsec%5Fkz%2FDocuments%2F%D0%A0%D0%B0%D0%B1%D0%BE%D1%87%D0%B8%D0%B9%20%D1%81%D1%82%D0%BE%D0%BB%2FTCOntent%2FAll%20Publications%20page%2FEN%2F2018%2Dyear%2Din%2Dreview%2Epdf&parent=%2Fpersonal%2Fn%5Fnudiyev%5Fnorsec%5Fkz%2FDocuments%2F%D0%A0%D0%B0%D0%B1%D0%BE%D1%87%D0%B8%D0%B9%20%D1%81%D1%82%D0%BE%D0%BB%2FTCOntent%2FAll%20Publications%20page%2FEN',
          },
          {
            name: '2019-20-corporate-responsibility-report.pdf',
            link: 'https://norsecdeltaprojects-my.sharepoint.com/personal/n_nudiyev_norsec_kz/_layouts/15/onedrive.aspx?ga=1&id=%2Fpersonal%2Fn%5Fnudiyev%5Fnorsec%5Fkz%2FDocuments%2F%D0%A0%D0%B0%D0%B1%D0%BE%D1%87%D0%B8%D0%B9%20%D1%81%D1%82%D0%BE%D0%BB%2FTCOntent%2FAll%20Publications%20page%2FEN%2F2019%2D20%2Dcorporate%2Dresponsibility%2Dreport%2Epdf&parent=%2Fpersonal%2Fn%5Fnudiyev%5Fnorsec%5Fkz%2FDocuments%2F%D0%A0%D0%B0%D0%B1%D0%BE%D1%87%D0%B8%D0%B9%20%D1%81%D1%82%D0%BE%D0%BB%2FTCOntent%2FAll%20Publications%20page%2FEN',
          },
          {
            name: '2019-year-in-review.pdf',
            link: 'https://norsecdeltaprojects-my.sharepoint.com/personal/n_nudiyev_norsec_kz/_layouts/15/onedrive.aspx?ga=1&id=%2Fpersonal%2Fn%5Fnudiyev%5Fnorsec%5Fkz%2FDocuments%2F%D0%A0%D0%B0%D0%B1%D0%BE%D1%87%D0%B8%D0%B9%20%D1%81%D1%82%D0%BE%D0%BB%2FTCOntent%2FAll%20Publications%20page%2FEN%2F2019%2Dyear%2Din%2Dreview%2Epdf&parent=%2Fpersonal%2Fn%5Fnudiyev%5Fnorsec%5Fkz%2FDocuments%2F%D0%A0%D0%B0%D0%B1%D0%BE%D1%87%D0%B8%D0%B9%20%D1%81%D1%82%D0%BE%D0%BB%2FTCOntent%2FAll%20Publications%20page%2FEN',
          },
          {
            name: '2021-corporate-responsibility-report.pdf',
            link: 'https://norsecdeltaprojects-my.sharepoint.com/personal/n_nudiyev_norsec_kz/_layouts/15/onedrive.aspx?ga=1&id=%2Fpersonal%2Fn%5Fnudiyev%5Fnorsec%5Fkz%2FDocuments%2F%D0%A0%D0%B0%D0%B1%D0%BE%D1%87%D0%B8%D0%B9%20%D1%81%D1%82%D0%BE%D0%BB%2FTCOntent%2FAll%20Publications%20page%2FEN%2F2021%2Dcorporate%2Dresponsibility%2Dreport%2Epdf&parent=%2Fpersonal%2Fn%5Fnudiyev%5Fnorsec%5Fkz%2FDocuments%2F%D0%A0%D0%B0%D0%B1%D0%BE%D1%87%D0%B8%D0%B9%20%D1%81%D1%82%D0%BE%D0%BB%2FTCOntent%2FAll%20Publications%20page%2FEN',
          },
          {
            name: 'egilik-brochure.pdf',
            link: 'https://norsecdeltaprojects-my.sharepoint.com/personal/n_nudiyev_norsec_kz/_layouts/15/onedrive.aspx?ga=1&id=%2Fpersonal%2Fn%5Fnudiyev%5Fnorsec%5Fkz%2FDocuments%2F%D0%A0%D0%B0%D0%B1%D0%BE%D1%87%D0%B8%D0%B9%20%D1%81%D1%82%D0%BE%D0%BB%2FTCOntent%2FAll%20Publications%20page%2FEN%2Fegilik%2Dbrochure%20%282%29%2Epdf&parent=%2Fpersonal%2Fn%5Fnudiyev%5Fnorsec%5Fkz%2FDocuments%2F%D0%A0%D0%B0%D0%B1%D0%BE%D1%87%D0%B8%D0%B9%20%D1%81%D1%82%D0%BE%D0%BB%2FTCOntent%2FAll%20Publications%20page%2FEN',
          },
          {
            name: 'environmental-brochure-eng.pdf',
            link: 'https://norsecdeltaprojects-my.sharepoint.com/personal/n_nudiyev_norsec_kz/_layouts/15/onedrive.aspx?ga=1&id=%2Fpersonal%2Fn%5Fnudiyev%5Fnorsec%5Fkz%2FDocuments%2F%D0%A0%D0%B0%D0%B1%D0%BE%D1%87%D0%B8%D0%B9%20%D1%81%D1%82%D0%BE%D0%BB%2FTCOntent%2FAll%20Publications%20page%2FEN%2Fenvironmental%2Dbrochure%2Deng%2Epdf&parent=%2Fpersonal%2Fn%5Fnudiyev%5Fnorsec%5Fkz%2FDocuments%2F%D0%A0%D0%B0%D0%B1%D0%BE%D1%87%D0%B8%D0%B9%20%D1%81%D1%82%D0%BE%D0%BB%2FTCOntent%2FAll%20Publications%20page%2FEN',
          },
          {
            name: 'feedback-management-process-flyer.pdf',
            link: 'https://norsecdeltaprojects-my.sharepoint.com/personal/n_nudiyev_norsec_kz/_layouts/15/onedrive.aspx?ga=1&id=%2Fpersonal%2Fn%5Fnudiyev%5Fnorsec%5Fkz%2FDocuments%2F%D0%A0%D0%B0%D0%B1%D0%BE%D1%87%D0%B8%D0%B9%20%D1%81%D1%82%D0%BE%D0%BB%2FTCOntent%2FAll%20Publications%20page%2FEN%2Ffeedback%2Dmanagement%2Dprocess%2Dflyer%2Epdf&parent=%2Fpersonal%2Fn%5Fnudiyev%5Fnorsec%5Fkz%2FDocuments%2F%D0%A0%D0%B0%D0%B1%D0%BE%D1%87%D0%B8%D0%B9%20%D1%81%D1%82%D0%BE%D0%BB%2FTCOntent%2FAll%20Publications%20page%2FEN',
          },
          {
            name: 'iv_kazcont_eng_2017.pdf',
            link: 'https://norsecdeltaprojects-my.sharepoint.com/personal/n_nudiyev_norsec_kz/_layouts/15/onedrive.aspx?ga=1&id=%2Fpersonal%2Fn%5Fnudiyev%5Fnorsec%5Fkz%2FDocuments%2F%D0%A0%D0%B0%D0%B1%D0%BE%D1%87%D0%B8%D0%B9%20%D1%81%D1%82%D0%BE%D0%BB%2FTCOntent%2FAll%20Publications%20page%2FEN%2Fiv%5Fkazcont%5Feng%5F2017%2Epdf&parent=%2Fpersonal%2Fn%5Fnudiyev%5Fnorsec%5Fkz%2FDocuments%2F%D0%A0%D0%B0%D0%B1%D0%BE%D1%87%D0%B8%D0%B9%20%D1%81%D1%82%D0%BE%D0%BB%2FTCOntent%2FAll%20Publications%20page%2FEN',
          },
          {
            name: 'tco_2015_2016_corporate-responsibility-report.pdf',
            link: 'https://norsecdeltaprojects-my.sharepoint.com/personal/n_nudiyev_norsec_kz/_layouts/15/onedrive.aspx?ga=1&id=%2Fpersonal%2Fn%5Fnudiyev%5Fnorsec%5Fkz%2FDocuments%2F%D0%A0%D0%B0%D0%B1%D0%BE%D1%87%D0%B8%D0%B9%20%D1%81%D1%82%D0%BE%D0%BB%2FTCOntent%2FAll%20Publications%20page%2FEN%2Ftco%5F2015%5F2016%5Fcorporate%2Dresponsibility%2Dreport%5Fe%2Epdf&parent=%2Fpersonal%2Fn%5Fnudiyev%5Fnorsec%5Fkz%2FDocuments%2F%D0%A0%D0%B0%D0%B1%D0%BE%D1%87%D0%B8%D0%B9%20%D1%81%D1%82%D0%BE%D0%BB%2FTCOntent%2FAll%20Publications%20page%2FEN',
          },
          {
            name: 'tco-2017-corporate-responsibility-report.pdf',
            link: 'https://norsecdeltaprojects-my.sharepoint.com/personal/n_nudiyev_norsec_kz/_layouts/15/onedrive.aspx?ga=1&id=%2Fpersonal%2Fn%5Fnudiyev%5Fnorsec%5Fkz%2FDocuments%2F%D0%A0%D0%B0%D0%B1%D0%BE%D1%87%D0%B8%D0%B9%20%D1%81%D1%82%D0%BE%D0%BB%2FTCOntent%2FAll%20Publications%20page%2FEN%2Ftco%2D2017%2Dcorporate%2Dresponsibility%2Dreport%2Epdf&parent=%2Fpersonal%2Fn%5Fnudiyev%5Fnorsec%5Fkz%2FDocuments%2F%D0%A0%D0%B0%D0%B1%D0%BE%D1%87%D0%B8%D0%B9%20%D1%81%D1%82%D0%BE%D0%BB%2FTCOntent%2FAll%20Publications%20page%2FEN',
          },
        ],
        kk: [
          {
            name: '2017-csrr-kz.pdf',
            link: 'https://norsecdeltaprojects-my.sharepoint.com/personal/n_nudiyev_norsec_kz/_layouts/15/onedrive.aspx?ga=1&id=%2Fpersonal%2Fn%5Fnudiyev%5Fnorsec%5Fkz%2FDocuments%2F%D0%A0%D0%B0%D0%B1%D0%BE%D1%87%D0%B8%D0%B9%20%D1%81%D1%82%D0%BE%D0%BB%2FTCOntent%2FAll%20Publications%20page%2FKAZ%2F2017%2Dcsrr%2Dkz%2Epdf&parent=%2Fpersonal%2Fn%5Fnudiyev%5Fnorsec%5Fkz%2FDocuments%2F%D0%A0%D0%B0%D0%B1%D0%BE%D1%87%D0%B8%D0%B9%20%D1%81%D1%82%D0%BE%D0%BB%2FTCOntent%2FAll%20Publications%20page%2FKAZ',
          },
          {
            name: '2017-??????-??????????????????????????.pdf',
            link: 'https://norsecdeltaprojects-my.sharepoint.com/personal/n_nudiyev_norsec_kz/_layouts/15/onedrive.aspx?ga=1&id=%2Fpersonal%2Fn%5Fnudiyev%5Fnorsec%5Fkz%2FDocuments%2F%D0%A0%D0%B0%D0%B1%D0%BE%D1%87%D0%B8%D0%B9%20%D1%81%D1%82%D0%BE%D0%BB%2FTCOntent%2FAll%20Publications%20page%2FKAZ%2F2017%2D%D0%B6%D1%8B%D0%BB%2D%D2%9B%D0%BE%D1%80%D1%8B%D1%82%D1%8B%D0%BD%D0%B4%D1%8B%D0%BB%D0%B0%D1%80%D1%8B%2Epdf&parent=%2Fpersonal%2Fn%5Fnudiyev%5Fnorsec%5Fkz%2FDocuments%2F%D0%A0%D0%B0%D0%B1%D0%BE%D1%87%D0%B8%D0%B9%20%D1%81%D1%82%D0%BE%D0%BB%2FTCOntent%2FAll%20Publications%20page%2FKAZ',
          },
          {
            name: '2018-corporate-responsibility-report (1).pdf',
            link: 'https://norsecdeltaprojects-my.sharepoint.com/personal/n_nudiyev_norsec_kz/_layouts/15/onedrive.aspx?ga=1&id=%2Fpersonal%2Fn%5Fnudiyev%5Fnorsec%5Fkz%2FDocuments%2F%D0%A0%D0%B0%D0%B1%D0%BE%D1%87%D0%B8%D0%B9%20%D1%81%D1%82%D0%BE%D0%BB%2FTCOntent%2FAll%20Publications%20page%2FKAZ%2F2018%2Dcorporate%2Dresponsibility%2Dreport%20%281%29%2Epdf&parent=%2Fpersonal%2Fn%5Fnudiyev%5Fnorsec%5Fkz%2FDocuments%2F%D0%A0%D0%B0%D0%B1%D0%BE%D1%87%D0%B8%D0%B9%20%D1%81%D1%82%D0%BE%D0%BB%2FTCOntent%2FAll%20Publications%20page%2FKAZ',
          },
          {
            name: '2018-??????-??????????????????????????.pdf',
            link: 'https://norsecdeltaprojects-my.sharepoint.com/personal/n_nudiyev_norsec_kz/_layouts/15/onedrive.aspx?ga=1&id=%2Fpersonal%2Fn%5Fnudiyev%5Fnorsec%5Fkz%2FDocuments%2F%D0%A0%D0%B0%D0%B1%D0%BE%D1%87%D0%B8%D0%B9%20%D1%81%D1%82%D0%BE%D0%BB%2FTCOntent%2FAll%20Publications%20page%2FKAZ%2F2018%2D%D0%B6%D1%8B%D0%BB%2D%D2%9B%D0%BE%D1%80%D1%8B%D1%82%D1%8B%D0%BD%D0%B4%D1%8B%D0%BB%D0%B0%D1%80%D1%8B%2Epdf&parent=%2Fpersonal%2Fn%5Fnudiyev%5Fnorsec%5Fkz%2FDocuments%2F%D0%A0%D0%B0%D0%B1%D0%BE%D1%87%D0%B8%D0%B9%20%D1%81%D1%82%D0%BE%D0%BB%2FTCOntent%2FAll%20Publications%20page%2FKAZ',
          },
          {
            name: '2019-20-????????????????????????-??????????????????????????-??????????????????????????-????????????-????????.pdf',
            link: 'https://norsecdeltaprojects-my.sharepoint.com/personal/n_nudiyev_norsec_kz/_layouts/15/onedrive.aspx?ga=1&id=%2Fpersonal%2Fn%5Fnudiyev%5Fnorsec%5Fkz%2FDocuments%2F%D0%A0%D0%B0%D0%B1%D0%BE%D1%87%D0%B8%D0%B9%20%D1%81%D1%82%D0%BE%D0%BB%2FTCOntent%2FAll%20Publications%20page%2FKAZ%2F2019%2D20%2D%D0%B6%D1%8B%D0%BB%D0%B4%D0%B0%D1%80%D1%8B%D0%BD%D0%B4%D0%B0%D2%93%D1%8B%2D%D0%BA%D0%BE%D1%80%D0%BF%D0%BE%D1%80%D0%B0%D1%82%D0%B8%D0%B2%D1%82%D1%96%D0%BA%2D%D0%B6%D0%B0%D1%83%D0%B0%D0%BF%D0%BA%D0%B5%D1%80%D1%88%D1%96%D0%BB%D1%96%D0%BA%2D%D1%82%D1%83%D1%80%D0%B0%D0%BB%D1%8B%2D%D0%B5%D1%81%D0%B5%D0%BF%2Epdf&parent=%2Fpersonal%2Fn%5Fnudiyev%5Fnorsec%5Fkz%2FDocuments%2F%D0%A0%D0%B0%D0%B1%D0%BE%D1%87%D0%B8%D0%B9%20%D1%81%D1%82%D0%BE%D0%BB%2FTCOntent%2FAll%20Publications%20page%2FKAZ',
          },
          {
            name: '2019-????????????-??????????????????????????.pdf',
            link: 'https://norsecdeltaprojects-my.sharepoint.com/personal/n_nudiyev_norsec_kz/_layouts/15/onedrive.aspx?ga=1&id=%2Fpersonal%2Fn%5Fnudiyev%5Fnorsec%5Fkz%2FDocuments%2F%D0%A0%D0%B0%D0%B1%D0%BE%D1%87%D0%B8%D0%B9%20%D1%81%D1%82%D0%BE%D0%BB%2FTCOntent%2FAll%20Publications%20page%2FKAZ%2F2019%2D%D0%B6%D1%8B%D0%BB%D0%B4%D1%8B%D2%A3%2D%D2%9B%D0%BE%D1%80%D1%8B%D1%82%D1%8B%D0%BD%D0%B4%D1%8B%D0%BB%D0%B0%D1%80%D1%8B%2Epdf&parent=%2Fpersonal%2Fn%5Fnudiyev%5Fnorsec%5Fkz%2FDocuments%2F%D0%A0%D0%B0%D0%B1%D0%BE%D1%87%D0%B8%D0%B9%20%D1%81%D1%82%D0%BE%D0%BB%2FTCOntent%2FAll%20Publications%20page%2FKAZ',
          },
          {
            name: '2021-??????????-??????????????-??????????????????????-??????????????????????????.pdf',
            link: 'https://norsecdeltaprojects-my.sharepoint.com/personal/n_nudiyev_norsec_kz/_layouts/15/onedrive.aspx?ga=1&id=%2Fpersonal%2Fn%5Fnudiyev%5Fnorsec%5Fkz%2FDocuments%2F%D0%A0%D0%B0%D0%B1%D0%BE%D1%87%D0%B8%D0%B9%20%D1%81%D1%82%D0%BE%D0%BB%2FTCOntent%2FAll%20Publications%20page%2FKAZ%2F2021%2D%D0%B6%D1%8B%D0%BB%D2%93%D1%8B%2D%D0%BD%D0%B5%D0%B3%D1%96%D0%B7%D0%B3%D1%96%2D%D1%8D%D0%BA%D0%BE%D0%BB%D0%BE%D0%B3%D0%B8%D1%8F%D0%BB%D1%8B%D2%9B%2D%D0%BA%D3%A9%D1%80%D1%81%D0%B5%D1%82%D0%BA%D1%96%D1%88%D1%82%D0%B5%D1%80%D1%96%2Epdf&parent=%2Fpersonal%2Fn%5Fnudiyev%5Fnorsec%5Fkz%2FDocuments%2F%D0%A0%D0%B0%D0%B1%D0%BE%D1%87%D0%B8%D0%B9%20%D1%81%D1%82%D0%BE%D0%BB%2FTCOntent%2FAll%20Publications%20page%2FKAZ',
          },
          {
            name: '2021-??????????????????????????-??????????????????????????-????????????-????????.pdf',
            link: 'https://norsecdeltaprojects-my.sharepoint.com/personal/n_nudiyev_norsec_kz/_layouts/15/onedrive.aspx?ga=1&id=%2Fpersonal%2Fn%5Fnudiyev%5Fnorsec%5Fkz%2FDocuments%2F%D0%A0%D0%B0%D0%B1%D0%BE%D1%87%D0%B8%D0%B9%20%D1%81%D1%82%D0%BE%D0%BB%2FTCOntent%2FAll%20Publications%20page%2FKAZ%2F2021%2D%D0%BA%D0%BE%D1%80%D0%BF%D0%BE%D1%80%D0%B0%D1%82%D0%B8%D0%B2%D1%82%D1%96%D0%BA%2D%D0%B6%D0%B0%D1%83%D0%B0%D0%BF%D0%BA%D0%B5%D1%80%D1%88%D1%96%D0%BB%D1%96%D0%BA%2D%D1%82%D1%83%D1%80%D0%B0%D0%BB%D1%8B%2D%D0%B5%D1%81%D0%B5%D0%BF%2Epdf&parent=%2Fpersonal%2Fn%5Fnudiyev%5Fnorsec%5Fkz%2FDocuments%2F%D0%A0%D0%B0%D0%B1%D0%BE%D1%87%D0%B8%D0%B9%20%D1%81%D1%82%D0%BE%D0%BB%2FTCOntent%2FAll%20Publications%20page%2FKAZ',
          },
          {
            name: 'egilik_kz_2016_for_web (1).pdf',
            link: 'https://norsecdeltaprojects-my.sharepoint.com/personal/n_nudiyev_norsec_kz/_layouts/15/onedrive.aspx?ga=1&id=%2Fpersonal%2Fn%5Fnudiyev%5Fnorsec%5Fkz%2FDocuments%2F%D0%A0%D0%B0%D0%B1%D0%BE%D1%87%D0%B8%D0%B9%20%D1%81%D1%82%D0%BE%D0%BB%2FTCOntent%2FAll%20Publications%20page%2FKAZ%2Fegilik%5Fkz%5F2016%5Ffor%5Fweb%20%281%29%2Epdf&parent=%2Fpersonal%2Fn%5Fnudiyev%5Fnorsec%5Fkz%2FDocuments%2F%D0%A0%D0%B0%D0%B1%D0%BE%D1%87%D0%B8%D0%B9%20%D1%81%D1%82%D0%BE%D0%BB%2FTCOntent%2FAll%20Publications%20page%2FKAZ',
          },
          {
            name: 'feedback-management-process-flyer (1).pdf',
            link: 'https://norsecdeltaprojects-my.sharepoint.com/personal/n_nudiyev_norsec_kz/_layouts/15/onedrive.aspx?ga=1&id=%2Fpersonal%2Fn%5Fnudiyev%5Fnorsec%5Fkz%2FDocuments%2F%D0%A0%D0%B0%D0%B1%D0%BE%D1%87%D0%B8%D0%B9%20%D1%81%D1%82%D0%BE%D0%BB%2FTCOntent%2FAll%20Publications%20page%2FKAZ%2Ffeedback%2Dmanagement%2Dprocess%2Dflyer%20%281%29%2Epdf&parent=%2Fpersonal%2Fn%5Fnudiyev%5Fnorsec%5Fkz%2FDocuments%2F%D0%A0%D0%B0%D0%B1%D0%BE%D1%87%D0%B8%D0%B9%20%D1%81%D1%82%D0%BE%D0%BB%2FTCOntent%2FAll%20Publications%20page%2FKAZ',
          },
          {
            name: 'iv_kazcont_kaz_2017.pdf',
            link: 'https://norsecdeltaprojects-my.sharepoint.com/personal/n_nudiyev_norsec_kz/_layouts/15/onedrive.aspx?ga=1&id=%2Fpersonal%2Fn%5Fnudiyev%5Fnorsec%5Fkz%2FDocuments%2F%D0%A0%D0%B0%D0%B1%D0%BE%D1%87%D0%B8%D0%B9%20%D1%81%D1%82%D0%BE%D0%BB%2FTCOntent%2FAll%20Publications%20page%2FKAZ%2Fiv%5Fkazcont%5Fkaz%5F2017%2Epdf&parent=%2Fpersonal%2Fn%5Fnudiyev%5Fnorsec%5Fkz%2FDocuments%2F%D0%A0%D0%B0%D0%B1%D0%BE%D1%87%D0%B8%D0%B9%20%D1%81%D1%82%D0%BE%D0%BB%2FTCOntent%2FAll%20Publications%20page%2FKAZ',
          },
          {
            name: 'tco_2015_2016_corporate-responsibility-report_k.pdf',
            link: 'https://norsecdeltaprojects-my.sharepoint.com/personal/n_nudiyev_norsec_kz/_layouts/15/onedrive.aspx?ga=1&id=%2Fpersonal%2Fn%5Fnudiyev%5Fnorsec%5Fkz%2FDocuments%2F%D0%A0%D0%B0%D0%B1%D0%BE%D1%87%D0%B8%D0%B9%20%D1%81%D1%82%D0%BE%D0%BB%2FTCOntent%2FAll%20Publications%20page%2FKAZ%2Ftco%5F2015%5F2016%5Fcorporate%2Dresponsibility%2Dreport%5Fk%2Epdf&parent=%2Fpersonal%2Fn%5Fnudiyev%5Fnorsec%5Fkz%2FDocuments%2F%D0%A0%D0%B0%D0%B1%D0%BE%D1%87%D0%B8%D0%B9%20%D1%81%D1%82%D0%BE%D0%BB%2FTCOntent%2FAll%20Publications%20page%2FKAZ',
          },
        ],
      },
    }
  },
}
</script>

<style lang="scss" scoped>
.p_block {
  padding-top: 80px;
  padding-bottom: 80px;
  @include tablet() {
    padding-top: 40px;
    padding-bottom: 40px;
  }
  &_title {
    display: flex;
    justify-content: space-between;
    align-items: center;
    @include tablet() {
      flex-direction: column;
      justify-content: flex-start;
      align-items: flex-start;
    }
    @media (orientation: portrait) {
      flex-direction: row;
      align-items: baseline;
      justify-content: space-between;
    }
    a {
      font-weight: 400;
      font-size: 20px;
      line-height: 28px;
      text-decoration-line: underline;
      color: #00b0f0;
      @include tablet() {
        font-size: 14px;
        line-height: 18px;
        margin-top: 12px;
      }
    }
  }
  &_list {
    display: grid;
    grid-template-columns: repeat(4, calc(25% - 18px));
    grid-gap: 24px;
    margin-top: 92px;
    @include tablet() {
      grid-template-columns: repeat(2, calc(50% - 7px));
      grid-gap: 13px;
      margin-top: 20px;
    }
  }
}
</style>
