<script>
	import Logo from './Logo.svelte'
	import Hamburger from './Hamburger.svelte'
	import Menu from './Menu.svelte'
	
	export let sidebar = false
</script>

<header class="flex">
	<nav class="flex">
		<Hamburger bind:open={sidebar}/>
		<Logo/>
		<Menu/>
	</nav>

</header>

<style>
	nav.flex {
		display: flex;
	}
</style>