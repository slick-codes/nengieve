<nav class="details flex">
	<ul class="details__container flex justify-between">
		<li>+234 805 498 5823</li>
		<li>Location: Somewere around Nigeria</li>
		<li>Mon - Fri: 8:00 - 5:00</li>
	</ul>
</nav>

<style lang="scss">
	/* your styles go here */
	@import './../styles/_config.scss';

	.details {
		justify-content: center;
		background: $background-white;

		&__container {
			width: 100%;
			padding: 0.6em 1em;
			max-width: $max-width;
		}
	}

	@media (max-width: 700px) {
		.details {
			display: none;
		}
	}
</style>
