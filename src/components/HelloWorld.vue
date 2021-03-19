<template>
  <div id="hello">
    时间：<input type="text" id="time" v-model="time" /><br>
    内容：<textarea id="article" v-model="article"></textarea><br>
    <button @click="add">确认</button>
  </div>
</template>
<script>
export default {
  name: 'HelloWord',
  props: {
    msg: String
  },
  data () {
    return {
      time: '',
      aeticle: ''
    }
  },
  methods: {
    add () {
      var that = this
      // console.log(this.time)
      // console.log(this.article)
      this.$axios.get('https://www.bbin.design/blog/blog_add.php', {
        params: {
          b_time: this.time,
          b_article: this.article
        }
      }).then((res) => {
        console.log(res.data)
        setTimeout(function () {
          alert('添加成功!')
          that.article = ''
        }, setTimeout(function () {
          that.$router.replace({ path: '/' })
        }, 3000), 1000)
      }).catch(req => {
        console.log(req)
      })
    }
  },
  created () {
    var that = this
    that.time = document.getElementById('time').innerHTML = new Date().toUTCString()
  }
}
</script>
<style scoped>
    #hello{
    text-align: center;
  }
  #time{
    width: 310px;
    margin-top: 30px;
  }
  #article{
    margin-top: 5px;
    width: 310px;
    height: 400px;
  }
</style>
