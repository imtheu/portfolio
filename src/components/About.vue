<template>
	<section id="about">
		<img src="../assets/sideArt.png" alt="" id="sideArt">
		<div class="mt-5 container text-center">
			<h1>About</h1>
			<div class="row">
				<div class="col-lg-4"></div>
				<div class="col-lg-8 about-text-column">
					<p class="about-text">Hi, my name is Matheus, I'm Brazilian and I'm 19 years old. I am currently studying Computer Science at the Pontifical Catholic University of Minas Gerais and I work as a developer at ABG Consultoria Estatística.</p>
				</div>
			</div>
			<div id="skills">
				<ul>
					<li><abbr title="PHP: Hypertext Preprocessor">PHP</abbr></li>
					<li title="C Programming language">C</li>
					<li title="Java programming language">Java</li>
					<li title="Node.js">Node.js</li>
					<li title="Javascript programming language">Javascript</li>
					<br>
					<li><abbr title="HyperText Markup Language">HTML</abbr></li>
					<li title="MySQL RDBMS">My<abbr title="Structured Query Language">SQL</abbr></li>
					<li title="CodeIgniter PHP Framework">CodeIgniter</li>
					<li title="Vue.js Javascript Framework">Vue.js</li>
					<br>
					<li><abbr title="Cascading Style Sheets">CSS</abbr></li>
					<li><abbr title="Syntactically Awesome Style Sheets">SASS</abbr></li>
					<li title="GIT Version Control System">GIT</li>
					<li title="Adobe applications">Adobe <abbr title="Creative Cloud">CC</abbr></li>
				</ul>
			</div>
		</div>
	</section>
</template>
<script>
	export default{
		name: 'About'
	}
</script>
<style scoped>
	#about{
		position: relative;
		padding-bottom: 50px;
		border-bottom: 1px dashed #eee;
	}
	#about *{
		font-family: Lato;
		color: #212121;
	}

	#sideArt{
		position: absolute;
		top: 80px;
		left: -60px;
	}

	h1{
		font-family: Lato;
		font-size: 60px;
		text-transform: uppercase;
		margin-top: 30px;
		display: inline-block;
	}

	abbr{
		text-decoration: none;
		color: #FFF!important;
		cursor: text;
	}
	.about-text{
		font-size: 24px;
		text-align: left;
		text-align: justify;
		justify-content: space-between;
	}

	.about-text-column{
		margin-top: 45px;
	}

	#skills ul{
		margin-top: 30px;
		padding: 0;
		display: block;
	}

	#skills ul li{
		list-style: none;
		padding: 15px 20px;
		display: inline-block;
		background: linear-gradient(123.42deg, #685C79 0%, #455C7B 100%);
		border-radius: 5px;
		font-size: 1.125em;
		color: #fff;
		margin: 7px 9px;
	}

	@media all and (max-width: 1200px){
		#sideArt{
			left: -200px;
		}
	}

	@media all and (max-width: 1000px){
		#sideArt{
			display: none;
		}	
		.col-lg-4{
			display: none;
		}
		.about-text-column{
			max-width: 100%!important;
			flex: 0 0 100%;
			margin-top: 10px;
		}

		#skills ul{
			margin-top: 10px;
		}
	}

	@media all and (max-width: 780px){
		#skills ul{
			margin-left: 0;
		}
		#skills ul br{
			display: none;
		}
		#skills ul li{
			margin-left: 0;
			font-size: 1em;
		}
	}
</style>