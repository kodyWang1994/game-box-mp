<template>
  <div class="abort-container">
    <div>
      <div style="text-align: center;font-size:22px;font-weight:600;">关于作品</div>
      <p>
        这个游戏集合是我平时利用空余时间边想边写，慢慢积累出来的（还在持续更新中，后续还会有新的游戏加入）。
        目的是为了更好的掌握前端相关知识和技能，同时也完成了我儿时的心愿（我终于也能写出来游戏了！！！），
        游戏界面超级简陋，没有任何美化，原谅我只有一双程序猿的手，没有一颗设计师的心，界面美化和交互设计只能等后面有空再整整了。
      </p>
      <p>大家玩的开心就好，欢迎提issue。</p>
      <p>源码地址：<span @click="copyLink" style="color:#49ab0c">https://github.com/kodyWang1994</span></p>
      <p>欢迎提意见报bug！谢谢大家！</p>
    </div>
  </div>
</template>

<script>
export default {
  methods: {
    copyLink () {
      wx.setClipboardData({
        data: 'https://github.com/kodyWang1994',
        success (res) {
          wx.showToast({
            title: '复制成功'
          })
        }
      })
    }
  }
}
</script>

<style scoped>
.abort-container {
  position: fixed;
  top: 0;
  bottom: 0;
  left: 0;
  right: 0;
  padding: 15px;
  background-color: #eee;
  overflow: scroll;
}

p {
  padding-top: 10px;
  text-indent: 30px;
  line-height: 2;
  font-size: 15px;
}
</style>
