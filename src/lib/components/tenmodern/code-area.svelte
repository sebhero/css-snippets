<script lang="ts">
	export let cssCode = '';
	export let htmlCode = '';

	const theStyle = `\<style` + ` style="display: block;" contenteditable="true">${cssCode}</style>`;

	let cssActive = true;

	const handleClick = () => {
		cssActive = !cssActive;
	};
</script>

<div class="code-area">
	<div class="tab-area">
		<button on:click={handleClick} class="tab html bg-gray-200 {!cssActive && 'active'}"
			>HTML</button
		>
		<button on:click={handleClick} class="tab css bg-gray-200 {cssActive && 'active'}">CSS</button>
	</div>
	<pre
		class="code-container  border-blue-400 border css {!cssActive &&
			'hidden'}">
	<!-- <code contenteditable="true">{cssCode}</code> -->
	{@html theStyle}
	</pre>
	<pre
		class="code-container border-blue-400 border html {cssActive &&
			'hidden'}">
        <code >{htmlCode}</code>
    </pre>
</div>

<style>
	.code-area {
		display: grid;
		grid-template-rows: auto 1fr auto;
		height: 400px;
	}

	.tab-area {
		display: grid;
		width: 50%;
		justify-self: end;
		grid-template-columns: 1fr 1fr;
	}

	.tab-area button.active {
		background-color: white;
		border: 1px solid var(--blue);
		border-bottom: none;
		z-index: 1;
	}

	.tab-area button {
		border: none;
		border-radius: 0.5rem 0.5rem 0 0;
		padding: 0.5rem;
	}

	.code-container {
		white-space: pre-wrap;
		overflow-y: scroll;
		background-color: var(--light-gray-blue);
		margin-bottom: 1rem;
		padding: 1rem;
		border: 1px solid var(--blue);
		margin-top: -1px;
		font-size: 1.35rem;
	}

	section:nth-child(2n) .code-container,
	section:nth-child(2n) .tab-area button.active {
		background-color: white;
	}
</style>
