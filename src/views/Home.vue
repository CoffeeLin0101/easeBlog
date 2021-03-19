<template>
    <div class="home">
        <HelloWord></HelloWord>
    </div>
</template>
<script>
import HelloWord from '../components/HelloWorld'
export default {
  name: 'Home',
  components: {
    HelloWord
  }

}
</script>
<style scoped>
  .home{
    margin-top: 80px;
  }
</style>
