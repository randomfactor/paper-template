<script lang="ts">
	import { Router, Link, Route } from "svelte-routing";

	export let open = false

	function hideSidebar() {
		open = false;
	}
</script>

<aside class="absolute border w-full h-full bg-gray-200 border-r-2 shadow-lg" class:open>
	<nav>
		<ul class="child-borders">
			<li><Link to="/" getProps="{hideSidebar}">Home</Link></li>
			<li><Link to="about">About</Link></li>
			<li><Link to="contact">Contact</Link></li>
		</ul>
	</nav>
</aside>

<style>
	aside {
		left: -90%;
		position: absolute;
		height: 100%;
		width: 90%;
		transition: left 0.3s ease-in-out
	}
	
	.open {
		left: 0
	}

	li {
		padding: 15px;
	}

</style>