<template>
    <div>
        <ul>
            <li v-for="items in list" :key="items">
                <div id="article">{{items.b_article}}</div>
                <div id="time">{{items.b_time}}</div>
            </li>
        </ul>
    </div>
</template>
<script>
export default {
  name: 'read',
  data () {
    return {
      list: ''
    }
  },
  mounted () {
    // var that = this
    console.log(123)
    this.$axios.get('https://www.bbin.design/blog/blog_add.php')
      .then((res) => {
        this.list = res.data
        console.log('123', res.data)
      }).catch(req => {
        console.log(req)
      })
  }
}
</script>
<style scoped>
    li{
        border-bottom: 1px solid blue;
        line-height: 50px;
    }
    #article{
        text-align: left;
        font-size: 20px;
    }
    #time{
        text-align: right;
        font-size: 15px;
        color: red;
    }
</style>
