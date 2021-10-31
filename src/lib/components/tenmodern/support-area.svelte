<script>
	export let EdgeColor = 'green';
	export let ChromeColor = 'green';
	export let FirefoxColor = 'green';
	export let SafariColor = 'green';
</script>

<div class="support-area pb-2">
	<span>Current Browser Support:</span>
	<ul class="taglist">
		<li class={EdgeColor}>Edge</li>
		<li class={ChromeColor}>Chrome</li>
		<li class={FirefoxColor}>Firefox</li>
		<li class={SafariColor}>Safari</li>
	</ul>
</div>

<style>
	.support-area {
		display: grid;
		justify-content: flex-end;
	}
	.support-area span {
		justify-self: flex-end;
		margin-bottom: 0.25rem;
	}
	.taglist {
		display: flex;
		gap: 0.2rem;
	}
	.taglist li {
		padding: 0.2rem 0.5rem;
		border-radius: 1rem;
		font-size: 14px;
		list-style: none;
	}
</style>
