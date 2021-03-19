<template>
    <div id="about">
        <read></read>
    </div>
</template>
<script>
import read from '../components/read'
export default {
  name: 'Me',
  components: {
    read
  }
}
</script>
<style scoped>
  #about{
    margin-top: 100px;
    text-align: center;
  }
</style>
