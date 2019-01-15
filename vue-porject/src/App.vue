<template>
  <div id="app">
    <el-container>
		  <el-header>
		  	<HeaderMain/>
		  </el-header>
		  <el-container>
		    <el-aside width="200px">左边栏</el-aside>
		    <el-main>
		    	<!--<router-view/>-->
		    </el-main>
		  </el-container>
		</el-container>
	</div>
</template>
<script>
	import HeaderMain from '@/components/Common/HeaderMain.vue';
	export default {
	  components: {
	    HeaderMain
	  }
	};
</script>
</script>
<style lang="stylus">
	body
		margin 0 auto
		font-family '微软雅黑'
	.el-header
		padding 0px !important;
		background #5D9CEC
/*#app
  font-family 'Avenir', Helvetica, Arial, sans-serif
  -webkit-font-smoothing antialiased
  -moz-osx-font-smoothing grayscale
  text-align center
  color #2c3e50

#nav
  padding 30px
  a
    font-weight bold
    color #2c3e50
    &.router-link-exact-active
      color #42b983*/
</style>
