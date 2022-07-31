<script>
	import ContactDetailsNav from './../components/ContactDetailsNav.svelte'
	import Nav from '../components/Nav.svelte'

	export let segment
</script>

<main>
	<ContactDetailsNav />
	<Nav />
	<slot />
</main>

<style lang="scss" global>
	@import './../styles/main.scss';
</style>
