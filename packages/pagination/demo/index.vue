<template>
  <demo-section>
    <demo-block :title="$t('basicUsage')">
      <van-pagination
        v-model="currentPage1"
        :total-items="24"
        :items-per-page="5"
        :previous-text= "$t('prevText')"
        :next-text= "$t('nextText')"
      />
    </demo-block>

    <demo-block :title="$t('title2')">
      <van-pagination
        v-model="currentPage2"
        :page-count="12"
        :previous-text= "$t('prevText')"
        :next-text= "$t('nextText')"
        mode="simple"
        size="small"
      />
    </demo-block>

    <demo-block :title="$t('title3')">
      <van-pagination
        force-ellipses
        v-model="currentPage3"
        :total-items="125"
        :show-page-size="3"
        :previous-text= "$t('prevText')"
        :next-text= "$t('nextText')"
      />
    </demo-block>
  </demo-section>
</template>

<script>
export default {
  i18n: {
    'zh-CN': {
      title2: '简单模式',
      title3: '',
      prevText: '上一页',
      nextText: '下一页'
    },
    'en-US': {
      title2: 'Simple Mode',
      title3: 'Show ellipses',
      prevText: 'Prev',
      nextText: 'Next'
    }
  },

  data() {
    return {
      currentPage1: 1,
      currentPage2: 1,
      currentPage3: 1
    };
  }
};
</script>

<style lang="postcss">
.demo-pagination {
  .van-pagination {
    margin: 5px 0;
    width: 100%;
  }

  .van-doc-demo-block {
    padding: 0 15px;
  }

  .van-doc-demo-block__title {
    padding-left: 0;
  }
}
</style>
