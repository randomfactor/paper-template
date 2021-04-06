<script lang="ts">
	import { Router, Link, Route } from "svelte-routing";
	import Home from "./routes/Home.svelte";
	import About from "./routes/About.svelte";
	import Contact from "./routes/Contact.svelte";
	// import Blog from "./routes/Blog.svelte";
	import Navbar from './components/Navbar.svelte'
	import Sidebar from './components/Sidebar.svelte'
	import Main from './components/Main.svelte'

	let open = false

	export let url = "";
</script>

<Router url="{url}">
	<Navbar bind:sidebar={open}/>
	<Sidebar bind:open />
	<div>
<!--		<Route path="blog/:id" component="{BlogPost}" />-->
<!--		<Route path="blog" component="{Blog}" />-->
		<Route path="about" component="{About}" />
		<Route path="/"><Home name="Henry" /></Route>
		<Route path="contact" component="{Contact}" />
	</div>
</Router>
