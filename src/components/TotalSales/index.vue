<template>
  <common-card title="累计销售额" value="$ 32,039,165">
    <template>
      <div class="compare-wrapper">
        <div class="compare">
          <span>日同比</span>
          <span>7.33%</span>
          <div class="increase" />
        </div>
        <div class="compare">
          <span>月同比</span>
          <span>7.33%</span>
          <div class="decrease" />
        </div>
      </div>
    </template>
    <template v-slot:footer>
      <span>昨日销售额</span>
      <span class="emphasize">$ 30,000,000</span>
    </template>
  </common-card>
</template>

<script>
import commonCardMixin from '@/mixins/commonCardMixin'

export default {
  mixins: [commonCardMixin],
}
</script>

<style scoped lang="scss">
.compare-wrapper {
  height: 100%;
  display: flex;
  flex-direction: column;
  justify-content: center;

  .compare {
    display: flex;
    align-items: center;
    font-size: 12px;
    margin-top: 10px;
    color: #666;
  }
}
</style>
