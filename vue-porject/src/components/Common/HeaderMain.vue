<template>
	<div>
		<div class="HeaderLogo">
  			<img class="Logo" src="@/assets/headerLogo.png" alt="" />
	  		<span class="LogoText">区域基本公共卫生信息管理平台</span>
	  	</div>
		<el-menu
		  :default-active="activeIndex2"
		  class="el-menu-demo"
		  mode="horizontal"
		  @select="handleSelect"
		  background-color="#5D9CEC"
		  text-color="#fff"
		  active-text-color="#ffd04b"
		  >
			<el-menu-item index="1">{{timer}}</el-menu-item>
			<el-menu-item index="2">
				<img src="@/assets/icon/out.png" alt="" />
			</el-menu-item>
		</el-menu>
	</div>
</template>
<script>
    import dayjs from 'dayjs'
    export default {
	  	name: 'HeaderMain',
	    data() {
	      return {
	        activeIndex2: '1',
	        timer : null
	      };
	    },
	    created:function(){
	    	setInterval(this.timerFun, 1000);
	    },
	    methods: {
	    	timerFun: function () {
	            this.timer = dayjs().format('YYYY-MM-DD HH:mm:ss')
	        },
	        handleSelect(key, keyPath) {
	          	console.log(key, keyPath);
	        }
	    }
    }
</script>

<style scoped lang="stylus">
	.HeaderLogo
		float left
		height 60px
		line-height 60px
	.Logo
		width 35px
		padding 0px 10px
		vertical-align middle
	.LogoText
		font-size 20px
		font-weight bold	
		vertical-align: middle
		vertical-align middle
		color #fff
	.el-menu
		display inline-block
		float right
	.el-menu-item
		border-bottom none !important
</style>