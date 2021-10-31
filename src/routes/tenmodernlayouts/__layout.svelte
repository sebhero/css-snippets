<slot />

<style global lang="postcss">
	:root {
		--coral: hsl(23, 83%, 82%);
		--coral--b: hsl(23, 99%, 75%);
		--pink: hsl(335, 52%, 92%);
		--pink--b: hsl(335, 82%, 86%);
		--yellow: hsl(42, 97%, 85%);
		--yellow--b: hsl(42, 100%, 73%);
		--green: hsl(100, 64%, 86%);
		--green--b: hsl(100, 41%, 76%);
		--blue: hsl(187, 61%, 79%);
		--blue--b: hsl(187, 54%, 68%);
		--purple: hsl(283, 24%, 86%);
		--purple--b: hsl(283, 43%, 80%);
		--light-gray-blue: hsl(182, 29%, 96%);
	}

	section:nth-child(2n) {
		background-color: var(--light-gray-blue);
	}

	section:nth-child(2n) .code-container,
	section:nth-child(2n) .tab-area button.active {
		background-color: white;
	}

	.coral {
		background-color: var(--coral);
		border: 1px solid var(--coral--b);
	}

	.pink {
		background-color: var(--pink);
		border: 1px solid var(--pink--b);
	}

	.yellow {
		background-color: var(--yellow);
		border: 1px solid var(--yellow--b);
	}

	.green {
		background-color: var(--green);
		border: 1px solid var(--green--b);
	}

	.blue {
		background-color: var(--blue);
		border: 1px solid var(--blue--b);
	}

	.purple {
		background-color: var(--purple);
		border: 1px solid var(--purple--b);
	}

	.white {
		background-color: white;
	}

	h1 {
		font-size: initial;
		line-height: initial;
	}
</style>
