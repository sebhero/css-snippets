<script lang="ts">
	export let htmlCode = '';
	export let cssCode = '';

	const theStyle = `\<style` + ` style="display: block;" contenteditable="true">${cssCode}</style>`;
	// const theStyle = `
	// \<style\>${cssCode} ${standardStyle}
	// \<\/style\>`;
</script>

<div class="ex-area">
	<div class="ex-container">
		{@html htmlCode}
	</div>
</div>

<!-- {@html theStyle} -->
<style>
	.ex-container {
		resize: both;
		position: relative;
		overflow: hidden;
		height: 100%;
		width: 100%;
		z-index: 2;
		box-shadow: 0 0 20px -10px hsl(187, 97%, 24%);
		display: grid;
		align-items: center;
		background: white;
	}
	:global(.box) {
		font-size: 2rem;
		padding: 1rem;
		display: grid;
		place-items: center;
		border-radius: 1rem;
		border-style: dashed;
	}
	:global(.parent) {
		width: 100%;
		height: 100%;
	}

	:global(.section) {
		font-size: 1.5rem;
		padding: 1rem;
		border-style: dashed;
	}
</style>
