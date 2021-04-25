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
		left: -100%;
		position: absolute;
		height: 100%;
		width: 50%;
		transition: left 0.3s ease-in-out;
		background-color: white;
	}

	@media only screen and (max-width: 768px) {
		aside {
			width: 90%;
		}
	}
	
	.open {
		left: 0
	}

	li {
		margin-top: 15px;
		padding: 15px;
	}

	nav {
		display: block;
	}

	nav ul {
		text-align: center;
	}

</style>