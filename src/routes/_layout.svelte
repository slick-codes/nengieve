<script>
	import Nav from '../components/Nav.svelte'

	export let segment
</script>

<Nav {segment} />

<main>
	<slot />
</main>

<style lang="scss" global> 
	@import './../styles/main.scss';
</style>
