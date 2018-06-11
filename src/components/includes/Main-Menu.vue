<template>
	<nav id="main-menu">
		<a href="" id="close-menu" v-on:click="closeMenu">
			<img src="../../assets/times.svg" alt="Close menu">
		</a>
		<ul class="nav" id="links">
			<li class="active"><a href="/#hello">Hello</a></li>
			<li><a v-on:click="goTo('#about')" href="/#about">About</a></li>
			<li><a v-on:click="goTo('#works')" href="/#works">Works</a></li>
			<li><a v-on:click="goTo('#contact')" href="/#contact">Contact</a></li>
		</ul>
		<a href="" id="burger-menu" v-on:click="openMenu">
			<img src="../../assets/bars.svg" alt="Open menu">
		</a>
	</nav>
</template>

<script>

	export default {
		name: 'main-menu',
		methods: {
			openMenu: function(event){
				event.preventDefault();
				document.getElementById("main-menu").classList.add('mobile');
			},
			closeMenu: function(event){
				event.preventDefault();
				document.getElementById("main-menu").classList.remove('mobile');
			},
			goTo: function(where){
		    	$('html, body').animate({
		        	scrollTop: $(where).offset().top
		    	}, 1500);
		    	if($("#main-menu").hasClass("mobile")){
		    		document.getElementById("main-menu").classList.remove('mobile');
		    	}
			}
		}
	}

</script>

<style scoped>
	#main-menu{
		float: right;
		line-height: 178px;
	}
	#main-menu .nav li{
		padding: 5px;
		text-transform: uppercase;
		font-family: 'Lato', sans-serif;
		font-size: 1.25em;
	}
	#main-menu .nav li a{
		color: #FFF;
		text-decoration: none;
	}
	#main-menu .nav li.active{
		font-weight: 500;
	}
	#main-menu .nav li::after{
		content: '\2022';
		margin-left: 18px;
		margin-right: 18px;
		color: #D1A824;
	}

	#main-menu .nav li:last-child::after{
		content: '';
		margin-left: 0px;
		margin-right: 0px;
	}

	#close-menu{
		display: none;
	}

	#close-menu img{
		width: 40px;
	}

	#burger-menu{
		display: none;
	}

	#burger-menu img{
		width: 40px;
	}

	.mobile{
		display: block;
		position: fixed;
		top: 0;
		left: 0;
		background: #493A3B;
		width: 100vw;
		height: 100vh;
		line-height: normal!important;
		text-align: center;
	}

	.mobile .nav{
		margin-top: 130px;
		display: block!important;
	}

	.mobile .nav li{
		font-size: 2.0em;
	}

	.mobile .nav li::after{
		display: block;
		content: '\A \2022'!important;
		white-space: pre;
		margin-left: 0!important;
		margin-right: 0!important;
		margin-top: 0.5vh;
		margin-bottom: 2.0vh;
	}

	.mobile .nav li:last-child::after{
		content: ''!important;
		margin-left: 0px!important;
		margin-right: 0px!important;
	}

	.mobile #burger-menu{
		display: none;
	}

	.mobile #close-menu{
		position: absolute;
		right: 50px;
		top: 30px;
		display: block;
	}

	@media all and (max-width: 780px){
		#main-menu .nav{
			display: none;
			background: #493A3B;
		}
		#burger-menu{
			display: inline-block;
		}
	}
</style>