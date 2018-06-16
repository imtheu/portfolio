<template>
	<div class="hello" id="hello">
		<page-header></page-header>
		<section class="container clearfix" id="apresentacao">
			<div id="nomeDisplay" class="clearfix">
				<h1 id="nome" class="float-left">Matheus<br>Francisco</h1>
				<span id="bracket" class="float-right">}</span>
			</div>
			<span id="greeting">It's me, hello! ;D</span>
			
			<div class="about">
				<div class="about-1">
					<span>Full stack developer</span>
				</div>
				<br>
				<div class="about-2">
					<span>computer science student</span>
				</div>
			</div>
		</section>
		<div id="transicao"></div>
		<div style="background: #FAFAFA; width: 100%; height: 10px; margin-top: -5px;"></div>
	</div>
</template>

<script>

import pageHeader from './includes/Page-Header.vue'

export default {
	name: 'Hello',
	components: {
		pageHeader
	}
}
</script>

<style scoped>
	.hello{
		background: #212121 url(../assets/background.png) no-repeat;
		left: 0px;
		top: 0px;
		color: #fff;
		clear: both;
	}
	.hello *{
		font-family: Lato;
		font-style: normal;
		font-weight: 300;
		line-height: normal;
	}

	#apresentacao{
		margin-top: 0px;
	}

	#nomeDisplay{
		float: left;
	}

	#nome{
		font-size: 7.5em;
	}

	#bracket{
		font-size: 8.75em;
		line-height: 296px;
		position: relative;
		margin-left: 60px;
	}

	#greeting{
		font-size: 2.5em;
		color: #D1A824;
		line-height: 296px;
		margin-left: 60px;
	}

	.about{
		text-align: center;
		display: block;
	}

	.about div{
		padding: 12px 18px;
		background: #493A3B;
		display: inline-block;
	}

	.about div span{
		color: #D1A824;
		font-size: 2.5em;
		text-transform: lowercase;
	}

	.about-1{
		margin-right: 220px;
	}
	.about-2{
		margin-left: 120px;
	}

	#transicao{
		background: url(../assets/transicao.png) no-repeat;
		/*width: 100vw;*/
		height: 169px;
		margin-top: 40px;
	}

	@media all and (max-width: 1000px){
		#nome{
			font-size: 6.5em;
		}
		#greeting{
			display: none;
		}
		#bracket{
			line-height: 250px;
		}

		.about{
			text-align: left;
		}

		.about div span{
			font-size: 1.5em;
		}

		.about-1, .about-2{
			margin: 0;
		}

		.about div{
			display: inline-block;
		}
	}

	@media all and (max-width: 780px){
		#nomeDisplay{
			float: none;
		}

		#nome{
			font-size: 5.5em;
		}

		#bracket{
			display: none;
			line-height: 250px;
		}
	}
	@media all and (max-width: 440px){
		#nome{
			font-size: 3.8em;
		}
		.about-2{
			margin-top: 10px;
		}
	}

</style>