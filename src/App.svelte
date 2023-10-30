<script>
	import { Router, Route } from "svelte-routing";
	import Home from "./routes/Home.svelte";
	import About from "./routes/About.svelte";
	import Blog from "./routes/Blog.svelte";
	import BlogPost from './routes/Blogpost.svelte'

	export let url = "";
</script>

<Router {url}>
	<div>
		<Route path="/blog/:id" component={BlogPost} />
		<Route path="/blog" component={Blog} />
		<Route path="/about" component={About} />
		<Route path="/"><Home /></Route>
	</div>
</Router>