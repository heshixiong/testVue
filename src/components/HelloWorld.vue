<template>
  <div class="hello">
    <iframe style="width:100%;height: 1000px" src="http://www.test.com/doc/page/playback.asp"></iframe>
  </div>
</template>

<script>

export default {
  name: 'HelloWorld',
  created () {
    // 防止this的指向改变
    let self = this
    // 在window对象上暴露出一个变量，赋值一个函数
    window.a = () => {
      // 当iframe中的报表提交按钮点击之后，回调此方法
      self.changeNodeMsg()
    }
  },
  methods: {
    changeNodeMsg () {
      alert(0)
    }
  }
}
</script>
