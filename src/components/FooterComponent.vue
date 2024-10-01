<template>
  <footer>
    <div class="icp">
      <span>© 2024</span><a href="https://luoh.pages.dev/" target="_blank">落渐离</a>
      <button class="logo-btn" @click="toggleTips">小提示</button>
    </div>
  </footer>
  <!-- 小提示弹窗 -->
  <div class="tips-popup" :class="{ 'show': showTipsPopup }">
    <div class="popup-content">
      <span>为避免性能问题，建议不要连续做图</span>
      <span>建议经常<a href="/">刷新页面</a>优化性能</span>
      <span class="highlight"><strong>重要提示：请确保您的浏览器和设备性能良好</strong></span>
      <span>修改于<a href="https://github.com/JLinMr/Mini-Cover">MiniCover</a></span>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      showTipsPopup: false,
      icpNumber: process.env.VUE_APP_ICP_NUMBER
    };
  },
  methods: {
    toggleTips() {
      this.showTipsPopup = !this.showTipsPopup;

      if (this.showTipsPopup) {
        setTimeout(() => {
          this.showTipsPopup = false;
        }, 3000);
      }
    }
  }
};
</script>