<script lang="ts">
	export let title = 'the title';
	export let subCode = 'sub code';
</script>

<div class="meta-area">
	<h2 class="section-title font-serif">
		{title}
		<code class="bg-blue-500 font-sans">{subCode}</code>
	</h2>
	<slot />
</div>

<style>
	.meta-area {
		display: grid;
		grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
		align-items: center;
		margin-bottom: 1rem;
	}

	.section-title {
		display: flex;
		flex-direction: column;
		align-items: flex-start;
	}
	.section-title code {
		display: block;
		width: auto;
		font-size: 0.8em;
		margin-left: 2em;
	}
</style>
