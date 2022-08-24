<template>
  <common-card title="累计订单量" value="2,157,420">
    <template>
      <div id="total-orders-chart" :style="{ width: '100%', height: '100%' }" />
    </template>
    <template v-slot:footer>
      <span>昨日订单量</span>
      <span class="emphasize">2,000,000</span>
    </template>
  </common-card>
</template>

<script>
import commonCardMixin from '@/mixins/commonCardMixin'

export default {
  mixins: [commonCardMixin],
  mounted() {
    const chartDom = document.getElementById('total-orders-chart')
    const chart = this.$echarts.init(chartDom)

    chart.setOption({
      xAxis: {
        type: 'category',
        show: false, // 隐藏坐标系
        boundaryGap: false, // true：默认的时候会在左右两边有间距
      },
      yAxis: {
        show: false, // 隐藏坐标系
      },
      series: [
        {
          type: 'line',
          data: [
            620, 432, 220, 534, 790, 430, 220, 320, 532, 320, 834, 690, 530,
            220, 620,
          ],
          areaStyle: {
            color: 'purple',
          },
          // 线条
          lineStyle: {
            width: 0,
          },
          // 线条上的点
          itemStyle: {
            opacity: 0,
          },
          smooth: true,
        },
      ],
      grid: {
        top: 0,
        bottom: 0,
        left: 0,
        right: 0,
      },
    })
  },
}
</script>
