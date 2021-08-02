<template>
  <div id="app">
      <router-view></router-view>
    <TabBar></TabBar>
  </div>
</template>

<script>
    // import TabBar from './components/TabBar/Tab-Bar'
    // import TabBarItem from './components/TabBar/TabBarItem'
    import TabBar from '@/views/TabView'
export default {
  name: 'app',
  components: {
      TabBar
  }
}
</script>

<style>


</style>
