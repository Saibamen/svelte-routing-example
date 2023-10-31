<script>
import { Router, Link } from 'svelte-routing'
import Navigation from './Navigation.svelte';
</script>

<Router>
	<Navigation />
	<Navigation items={[
		{ text: "Batches list", url: "/batch/list/1" },
        { text: "Batch #1", url: "/batch/1" },
        { text: "Regenerate DATA files" },
	]} />
	<Link to="/">Home</Link>
	<Link to="/about">About</Link>
	<Link to="/blog">Blog</Link>
</Router>
