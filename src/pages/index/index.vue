<template>
  <div class="home-container">
    <div class="title">小游戏集合</div>
    <div class="menu-wrap">
      <!-- <div href="index.html#/snake" class="menu-item">贪吃蛇</div> -->
      <!-- <div href="index.html#/eliminate" class="menu-item">消消乐</div> -->
      <!-- <div href="index.html#/pop-block" class="menu-item">消灭方块</div> -->
      <!-- <div href="index.html#/drag-block" class="menu-item">拖动方块</div> -->
      <div @click="gotoPage('/pages/color/main')" class="menu-item">烧脑颜色</div>
      <!-- <div href="index.html#/pictire" class="menu-item">拼图</div> -->
      <div @click="gotoPage('/pages/number_eliminate/main')" class="menu-item">数字消消乐</div>
      <div @click="gotoPage('/pages/picture/main')" class="menu-item">自定义拼图</div>
      <!-- <div href="index.html#/draw" class="menu-item">画板</div> -->
      <!-- <div href="index.html#/date" class="menu-item">日历</div> -->
    </div>
    <div class="abort-us">
      <!-- <a href="/abort-us">关于作品</a> -->
      <a href="index.html#/abort-us">关于作品</a>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data () {
    return {
    }
  },
  methods: {
    gotoPage (page) {
      wx.navigateTo({
        url: page
      })
    }
  },
  onShareAppMessage (res) {
    return {
      title: '简单怀旧小游戏集合,快来一起玩吧！'
    }
  }
}
</script>

<style scoped>
.home-container{
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background-image: url('https://images.pexels.com/photos/18174/reflection-pad-gaming-gamepad.jpg?auto=compress&cs=tinysrgb&dpr=2&h=750&w=1260');
  background-repeat: no-repeat;
  background-position: center;
  background-size: cover;
  overflow: scroll;
}

.abort-us {
  padding: 20px;
  text-align: center;
}

.abort-us div {
  text-decoration-line: none;
  color: #333;
  text-shadow: #7777d8 2px 2px 10px;
}

.title {
  text-align: center;
  font-size: 28px;
  margin: 75px 0;
  color: #fff;
  text-shadow: #7777d8 2px 2px 10px;
}

.menu-wrap {
  width: 60%;
  margin: auto;
}

.menu-item {
  display: block;
  text-decoration-line: none;
  border-radius: 25px;
  background-color: #7777d8;
  height: 40px;
  line-height: 40px;
  margin-bottom: 15px;
  text-align: center;
  color: #fff;
  box-shadow: #7777d9 0 0 6px 0px;
}
</style>
