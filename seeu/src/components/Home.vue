<template>
  <div class="home">
    <!--Here will show you the tags in the home page-->
    <HeaderBar></HeaderBar>
    <NavigationBar></NavigationBar>
    <router-view/>
  </div>
</template>

<script>
import NavigationBar from "@/components/navigation-bar/navigation-bar"
import HeaderBar from "@/components/header-bar/header-bar"

export default {
  name: 'Home',
  components:{
    NavigationBar,HeaderBar
  },
  data () {
    return {
      msg: 'Welcome to Your Vue.js App'
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="stylus" scoped>
  .home{
    height:100%;
    
  }
</style>
