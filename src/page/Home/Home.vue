<template>
  <div>
    <div>demo1数据双向绑定</div>
    <div>{{msg}}</div>
    <input type="text" v-model='msg'>
  </div>
</template>

<script>
export default {
  name: 'Home',
  data () {
    return {
      msg: 'hello home'
    }
  }
}
</script>
