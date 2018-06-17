<template>
	<section id="works">
		<div class="mt-5 container text-center">
			<h1>Works</h1>
		</div>
		<div class="container mt-5">
			<article class="row" v-for="(project, index) in projects">
				<div class="col-md-5">
		    		<h1><router-link :to="'project/' + index">{{ project.Name }}</router-link></h1>
		    		<p>{{ project.Description }}</p>
		    		<ul class="tags">
		    			<li v-for="tag in project.Tags">
		    				#{{ tag }}
		    			</li>
		    		</ul>
		    		<div class="text-right">
		    			<router-link :to="'project/' + index" class="btn btn-sm">More info +</router-link>
		    			<a :href="project.url" target="_blank" class="btn btn-info btn-sm">Access ></a>
		    		</div>
		    	</div>
		    	<div class="col-md-7">
		    		<img class="img-fluid" :src="getImg(project.Imgs['0'])" :alt="project.Name" :title="project.Name">
		    	</div>
	  		</article>
		</div>
	</section>
</template>

<script>
	import data from '../data/data.json'
	export default{
		name: 'Works',
		data () {
			return {
				projects: []
			}
		},
		methods: {
			getImg: function(src){
				let images = require.context('../imgs/');
				return images('./' + src);
			}
		},
		created: function(){
			this.projects = data.Projects;
		},
	}

</script>

<style scoped>
	*{
		font-family: Lato;
	}

	h1{	
		font-size: 60px;
		text-transform: uppercase;
		margin-top: 30px;
		display: inline-block;
	}

	article{
		margin-bottom: 80px;
	}

	article h1{
		text-transform: none;
		margin: 0;
		/*margin-top: 20px;*/
		/*display: inline-block;*/
		display: initial;
		font-size: 92px;
	}

	article h1 a{
		color: #212121;
		text-decoration: none;
	}

	article p{
		font-size: 17px;
	}

	.tags{
		padding: 0;
		margin-bottom: 5px;
	}

	.tags li{
		list-style: none;
		display: inline-block;
		padding: 0 2px;
		font-weight: 300;
		font-size: 15px;
		color: #616161;
	}

	article img{
		width: 627px;
		box-shadow: 0px 0px 50px rgba(33, 33, 33, 0.05);
	}

	@media all and (max-width: 770px){
		article img{
			margin-top: 20px;
		}
	}
</style>