<template>
  <div>
    <div>demo1数据双向绑定</div>
    <div>{{msg}}</div>
    <input type="text" v-model='msg'>
    <div v-bind:title='tip' >
      demo2 鼠标悬停几秒钟查看此处动态绑定的提示信息！
    </div>
    <div>demo3 循环</div>
    <div  v-for="item in todos" :key="item.text">
      {{item.text}}
    </div>
    <div>demo4 条件</div>
    <div v-if='flag' class="redB">条件</div>
    <div>demo5 点击事件 改变条件</div>
    <div v-on:click='press' >按钮8</div>
<!--     <div @click='press' >按钮</div> -->
    <ul id="example">
      <li v-for="item in items">
        {{ item.message }}
      </li>
    </ul>
    <ul id="example1">
      <li v-for="(item,index) in items">
        {{ parentMessage }} - {{index}} - {{item.message}}
      </li>
    </ul>
  </div>
</template>
<script>
export default {
  data () {
    return {
      msg: 'hello home',
      tip: '提示',
      todos: [
        { text: '学习 JavaScript' },
        { text: '学习 Vue' },
        { text: '整个牛项目' }
      ],
      flag: false,
      parentMessage:'Parent',
      items:[
        {message:'Foo'},
        {message:'Bar'}
      ],

    }
  },
  methods: {
    press (event) {
      this.flag = !this.flag
    }
  }
}
</script>
<style >
  .redB {
    background: red;
  }
  #example{
    width: 80px;
    margin:0 auto;
  }
</style>
