<script>
	import Icon from '@iconify/svelte'
	// export const = ''
	let isNavVisible = false
	const toggleNavigation = () => (isNavVisible = !isNavVisible)
</script>

<nav class="navigation flex sticky  top-0 justify-center w-full">
	<div
		class="navigation__container flex items-center justify-between 
		w-full absolute bg-white mt-6 px-4 py-3"
	>
		<ul class="justify-center items-center">
			<li><img src="/images/logo.png" alt="Nengieve Official Logo" /></li>
		</ul>
		<ul
			class="nav__link-container font-bold md:static md:flex fixed top-0 right-0 flex items-center ml-9"
			class:hidden={!isNavVisible ? 'hidden' : ''}
		>
			<div class="nav__overlay" on:click={toggleNavigation} />
			<div
				class="nav__content flex md:flex-row flex-col md:py-0 py-3 justify-center items-center"
			>
				<li class="md:py-0 p-2 flex justify-center">
					<a href="/" class="uppercase text-sm">Home</a>
				</li>
				<li class="md:py-0 p-2 flex justify-center">
					<a href="/services" class="uppercase text-sm">services</a>
				</li>
				<li class="md:py-0 p-2 flex justify-center">
					<a href="/" class="uppercase text-sm">about</a>
				</li>
				<li class="md:py-0 p-2 flex justify-center">
					<a href="/" class="uppercase text-sm">contact</a>
				</li>
				<li class="md:py-0 p-2 flex justify-center">
					<a href="/" class="uppercase text-sm">faq</a>
				</li>
			</div>
		</ul>
		<ul class="hidden align-center justify-center md:flex">
			<div class="socialicon flex justify-center align-center">
				<li class="flex align-center">
					<a href="/" class="px-2">
						<Icon icon="fa-brands:twitter-square" />
					</a>
				</li>
				<li class="flex align-center">
					<a href="/" class="px-2">
						<Icon icon="ant-design:facebook-filled" />
					</a>
				</li>
				<li class="flex align-center">
					<a href="/" class="px-2">
						<Icon icon="akar-icons:linkedin-box-fill" />
					</a>
				</li>
			</div>
		</ul>
		<ul class="flex md:hidden text-xl" on:click={toggleNavigation}>
			<Icon icon="fluent:navigation-16-regular" />
		</ul>
	</div>
</nav>

<style lang="scss">
	@import './../styles/_config.scss';
	/* your styles go here */
	.navigation {
		width: 100%;

		&__container {
			width: 90%;
			max-width: $max-width;
			padding: 1em 6em;
			// background: blue;
		}

		@media (max-width: 768px) {
			.navigation {
				&__container {
					padding: 1em 3em;
				}
			}
			.nav__link-container {
				flex-flow: column;
				width: 100%;
				height: 100vh;

				.nav__overlay {
					width: 100%;
					position: fixed;
					height: 100vh;
					z-index: -1;
					background: #101e4b0d;
				}

				.nav__content {
					margin-top: 5.8em;
					width: 90%;
					max-width: $max-width;
					background: white;
				}
			}
		}
	}
</style>
