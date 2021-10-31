<script>
	import CodeArea from './code-area.svelte';
	import ExArea from './ex-area.svelte';

	import MetaArea from './meta-area.svelte';
	import SupportArea from './support-area.svelte';

	export let htmlCode = '';
	export let cssCode = '';

	export let title = '';
	export let subCode = '';
	export let ChromeColor = '';
	export let EdgeColor = '';
	export let FirefoxColor = '';
	export let SafariColor = '';

	export let exercise = '';
</script>

<section>
	<div class="section-container">
		<MetaArea {title} {subCode}>
			<SupportArea {ChromeColor} {EdgeColor} {FirefoxColor} {SafariColor} />
		</MetaArea>
		<div class="ex-section {exercise}">
			<ExArea {htmlCode} {cssCode} />
			<CodeArea {htmlCode} {cssCode} />
		</div>
	</div>
</section>

<style>
	.ex-section {
		height: 400px;
		display: grid;
		grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
		grid-gap: 2rem;
	}

	.section-container {
		padding: 8rem 4rem;
		max-width: 1260px;
		margin: 0 auto;
		padding: 4rem 2rem;
	}
</style>
