<template>
  <common-card title="累计销售额" value="$ 32,039,165">
    <template v-slot:footer>
      <span>昨日销售额</span>
      <span class="money">$ 30,000,000</span>
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
.money {
  margin-left: 5px;
  color: #333;
  font-weight: 700;
}
</style>
