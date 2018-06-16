<template>
	<section id="contact">
		<div class="container text-center">
			<h1>Contact</h1>

			<div id="email">
				<span id="oi">oi</span><span id="at">@</span><span id="domain">matheusf</span><span id="dotcom">.com</span>
			</div>

			<nav id="social-networks">
				<ul>
					<li><a href="https://www.instagram.com/imtheu" target="_blank"><img src="../assets/icons/instagram.png" alt=""></a></li>
					<li><a href="https://www.github.com/imtheu" target="_blank"><img src="../assets/icons/github.png" alt=""></a></li>
					<li><a href="https://www.twitter.com/imtheu" target="_blank"><img src="../assets/icons/twitter.png" alt=""></a></li>
					<li><a href="https://www.linkedin.com/in/imatheus" target="_blank"><img src="../assets/icons/linkedin.png" alt=""></a></li>
				</ul>
			</nav>
		</div>
	</section>
</template>
<script>
	export default{
		name: 'Contact'
	}
</script>
<style scoped>
	#contact{
		padding-top: 70px;
		padding-bottom: 50px;
	}

	*{
		font-family: Lato;
	}

	h1{	
		font-size: 60px;
		text-transform: uppercase;
		margin-top: 30px;
		display: inline-block;
	}

	#email{
		font-size: 5em;
		margin-top: 25px;
	}

	#email #oi{
		color: #DA727E;
	}

	#email #at{
		color: #AC6C82;
	}

	#email #domain{
		color: #685C79;
	}

	#email #dotcom{
		color: #455C7B;
	}

	ul{
		padding: 0;
	}

	#social-networks{
		margin: 35px 0;
	}

	#social-networks ul li{
		display: inline-block;
		list-style: none;
		margin: 0 45px;
	}

	@media all and (max-width: 780px){
		#email{
			font-size: 2.5em;
		}
		#social-networks ul li{
			margin: 0 22px;
		}
		#social-networks ul li a img{
			width: 30px;
		}
	}

	@media all and (max-width: 360px) {
		#email{
			font-size: 2em;
		}
		#social-networks ul li{
			margin: 0 16px;
		}
		#social-networks ul li a img{
			width: 25px;
		}
	}
</style>