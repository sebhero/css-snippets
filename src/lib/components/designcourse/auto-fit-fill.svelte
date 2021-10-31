<div class="container grid-cols-6 p-4">
	<div class="quote span-2">
		<p>
			Lorem ipsum dolor sit amet, consectetur adipisicing elit.
			Adipisci dolores sunt repudiandae aspernatur veniam nihil?
		</p>
		<img
			class="w-full"
			src="https://dummyimage.com/200x150.png"
			alt=""
		/>

		<span>John Doe</span>
	</div>
	<div class="quote span-2">
		<p>
			Lorem ipsum dolor sit amet, consectetur adipisicing elit.
			Adipisci dolores sunt repudiandae aspernatur veniam nihil?
		</p>
		<img
			class="w-full"
			src="https://dummyimage.com/200x150.png"
			alt=""
		/>
		<span>John Doe Lorem ipsum dolor sit amet.</span>
	</div>
	<div class="quote span-2">
		<p>Lorem ipsum dolor sit amet.</p>
		<img
			class="w-full"
			src="https://dummyimage.com/200x150.png"
			alt=""
		/>

		<span>John Doe</span>
	</div>
	<div class="quote span-2">
		<p />
		<img
			class="w-full"
			src="https://dummyimage.com/200x150.png"
			alt=""
		/>

		<span>John Doe</span>
	</div>
	<div class="quote span-2">
		<p />
		<img
			class="w-full"
			src="https://dummyimage.com/200x150.png"
			alt=""
		/>

		<span
			>John Doe Lorem ipsum dolor sit amet consectetur adipisicing
			elit. Deleniti, molestiae?</span
		>
	</div>
	<div class="quote span-2">
		<p>
			Lorem ipsum dolor sit amet consectetur adipisicing elit.
			Doloremque, cupiditate.
		</p>
		<img
			class="w-full"
			src="https://dummyimage.com/200x150.png"
			alt=""
		/>

		<span>
			John Doe Lorem ipsum dolor sit amet consectetur adipisicing elit.
			Deleniti, molestiae
		</span>
	</div>
</div>

<style>
	:root {
		margin: 0;
	}
	.container {
		padding: 3em;
		display: grid;
		gap: 2em;
	}

	.container .quote {
		display: grid;
		grid-auto-rows: 1fr;

		padding: 2em;
		border-radius: 0.3em;
		box-shadow: 10px 10px 30px rgba(0, 0, 0, 0.1);
	}

	.container p {
		margin-top: 0;
	}
	.container span {
		font-weight: bold;
		position: relative;
		margin-left: 15px;
	}
	.container span:before {
		content: '';
		position: absolute;
		height: 1px;
		width: 10px;
		border-bottom: 1px solid black;
		top: 10px;
		left: -15px;
	}

	@media (min-width: 550px) {
		/* .span-2 {
			grid-column: auto / span 2;
		} */
	}
</style>
