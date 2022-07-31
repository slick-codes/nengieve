<script>
	import Icon from '@iconify/svelte'
	export const segment = ''
</script>

<nav class="navigation flex justify-center w-full">
	<div
		class="navigation__container flex items-center justify-between w-full absolute bg-white mt-6 p-2 px-4"
	>
		<ul class="justify-center items-center">
			<li>logo</li>
		</ul>
		<ul class="font-bold justify-center align-center">
			<a href="/" class="uppercase p-2 text-sm">Home</a>
			<a href="/" class="uppercase p-2 text-sm">services</a>
			<a href="/" class="uppercase p-2 text-sm">about</a>
			<a href="/" class="uppercase p-2 text-sm">contact</a>
			<a href="/" class="uppercase p-2 text-sm">faq</a>
		</ul>
		<ul class="flex align-center justify-center">
			<a href="/" class="p-2"> <Icon icon="fa-brands:twitter-square" /> </a>
			<a href="/" class="p-2"> <Icon icon="ant-design:facebook-filled" /> </a>
			<a href="/" class="p-2"> <Icon icon="akar-icons:linkedin-box-fill" /> </a>
		</ul>
	</div>
</nav>

<style lang="scss">
	@import './../styles/_config.scss';
	/* your styles go here */
	.navigation {
		width: 100%;

		&__container {
			max-width: $max-width;
			// background: blue;
		}
	}
</style>
