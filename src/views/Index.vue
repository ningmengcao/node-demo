<template>
  <div>
    <NavigationBar></NavigationBar>
    <Content></Content>
  </div>
</template>

<script>
import NavigationBar from '../components/NavigationBar/NavigationBar'
import Content from '../components/Content/Content'

export default {
  name: 'Index',
  components: {NavigationBar, Content}
}
</script>

<style scoped>

</style>
