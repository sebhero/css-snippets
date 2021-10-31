<script>
	import SectionContainer from '$lib/components/tenmodern/section-container.svelte';

	const htmlCodeEx1old = `
<div class="parent bg-blue-200 border border-blue-200">
	<div class="bg-yellow-300 text-lg p-4 rounded-2xl border-dashed border-gray-200" contenteditable>:)</div>
</div>
	`;
	const htmlCodeEx1 = `
    <div class="parent bg-blue-200" >
  <div class="box bg-yellow-300" contenteditable>
    :)
  </div>
	`;
	const cssCodeEx1 = `
    .ex1 .parent {
    display: grid;
    place-items: center;
  }
	`;
</script>

<div class="flex justify-center items-center">
	<h1 class="text-xl italic font-mono pr-2">From the site</h1>
	<a
		class="text-xl font-mono no-underline text-purple-800"
		href="https://1linelayouts.glitch.me/">1-line Layouts</a
	>
</div>

<SectionContainer
	title="01. Super Centered"
	subCode="place-items: center"
	ChromeColor="green"
	EdgeColor="green"
	FirefoxColor="green"
	SafariColor="green"
	exercise="ex1"
	htmlCode={htmlCodeEx1}
	cssCode={cssCodeEx1}
/>
<SectionContainer
	title="02. The Deconstructed Pancake "
	subCode="flex: 0 1 <baseWidth>"
	ChromeColor="green"
	EdgeColor="green"
	FirefoxColor="green"
	SafariColor="green"
	exercise="ex2"
	htmlCode={`
    <div class="parent white">
    <div class="box green">1</div>
    <div class="box green">2</div>
    <div class="box green">3</div>
  </div>`}
	cssCode={`
  .ex2 .parent {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
  }

  .ex2 .box {
    flex: 1 1 150px; /*  Stretching: */
    flex: 0 1 150px; /*  No stretching: */
    margin: 5px;
  }`}
/>

<SectionContainer
	title="03. Sidebar Says"
	subCode="grid-template-columns: minmax(<min>, <max>) ..."
	ChromeColor="green"
	EdgeColor="green"
	FirefoxColor="green"
	SafariColor="green"
	exercise="ex3"
	htmlCode={`
<div class="parent">
    <div class="section yellow" contenteditable>
    Min: 150px / Max: 25%
    </div>
    <div class="section purple" contenteditable>
      This element takes the second grid position (1fr), meaning
      it takes up the rest of the remaining space.
    </div>
  </div>`}
	cssCode={`
  .ex3 .parent {
    display: grid;
    grid-template-columns: minmax(150px, 25%) 1fr;
  }`}
/>

<SectionContainer
	title="04. Pancake Stack"
	subCode="grid-template-rows: auto 1fr auto"
	ChromeColor="green"
	EdgeColor="green"
	FirefoxColor="green"
	SafariColor="green"
	exercise="ex4"
	htmlCode={`
<div class="parent">
    <header class="blue section" contenteditable>Header</header>
    <main class="coral section" contenteditable>Main</main>
    <footer class="purple section" contenteditable>Footer Content</footer>
  </div>`}
	cssCode={`
.ex4 .parent {
    display: grid;
    grid-template-rows: auto 1fr auto;
  }`}
/>

<SectionContainer
	title="05. Classic Holy Grail Layout"
	subCode="grid-template: auto 1fr auto / auto 1fr auto"
	ChromeColor="green"
	EdgeColor="green"
	FirefoxColor="green"
	SafariColor="green"
	exercise="ex5"
	htmlCode={`
  <div class="parent">
    <header class="pink section">Header</header>
    <div class="left-side blue section" contenteditable>Left Sidebar</div>
    <main class="section coral" contenteditable> Main Content</main>
    <div class="right-side yellow section" contenteditable>Right Sidebar</div>
    <footer class="green section">Footer</footer>
  </div>`}
	cssCode={`

.ex5 .parent {
    display: grid;
    grid-template: auto 1fr auto / auto 1fr auto;
  }
  
  .ex5 header {
    padding: 2rem;
    grid-column: 1 / 4;
  }

  .ex5 .left-side {
    grid-column: 1 / 2;
  }

  .ex5 main {
    grid-column: 2 / 3;
  }

  .ex5 .right-side {
    grid-column: 3 / 4;
  }

  .ex5 footer {
    grid-column: 1 / 4;
  }`}
/>

<SectionContainer
	title="06. 12-Span Grid"
	subCode="grid-template-columns: repeat(12, 1fr)"
	ChromeColor="green"
	EdgeColor="green"
	FirefoxColor="green"
	SafariColor="green"
	exercise="ex6"
	htmlCode={`
  <div class="parent white">
    <div class="span-12 green section">Span 12</div>
    <div class="span-6 coral section">Span 6</div>
    <div class="span-4 blue section">Span 4</div>
    <div class="span-2 yellow section">Span 2</div>
  </div>`}
	cssCode={`
        .ex6 .parent {
          display: grid;
          grid-template-columns: repeat(12, 1fr);
        }
        
        .ex6 .span-12 {
          grid-column: 1 / span 12;
        }
      
        .ex6 .span-6 {
          grid-column: 1 / span 6;
        }
      
        .ex6 .span-4 {
          grid-column: 4 / span 4;
        }
      
        .ex6 .span-2 {
          grid-column: 3 / span 2;
        }
      
        /* centering text */
        .ex6 .section {
          display: grid;
          place-items: center;
          text-align: center
        }`}
/>

<!-- 7 -->
<SectionContainer
	title="07. RAM (Repeat, Auto, Minmax)"
	subCode="grid-template-columns: repeat(auto-fit, minmax(<base>, 1fr))"
	ChromeColor="green"
	EdgeColor="green"
	FirefoxColor="green"
	SafariColor="green"
	exercise="ex7"
	htmlCode={`
  <div class="parent white">
    <div class="box pink">1</div>
    <div class="box purple">2</div>
    <div class="box blue">3</div>
    <div class="box green">4</div>
  </div>`}
	cssCode={`
  .ex7 .parent {
    display: grid;
    grid-gap: 1rem;
    grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
  }`}
/>

<!-- 8 -->
<SectionContainer
	title="08. Line Up"
	subCode="justify-content: space-between"
	ChromeColor="green"
	EdgeColor="green"
	FirefoxColor="green"
	SafariColor="green"
	exercise="ex8"
	htmlCode={`
    <div class="parent white">
    <div class="card yellow">
      <h3>Title - Card 1</h3>
      <p contenteditable>Medium length description with a few more words here.</p>
      <div class="visual pink"></div>
    </div>
    <div class="card yellow">
      <h3>Title - Card 2</h3>
      <p contenteditable>Long Description. Lorem ipsum dolor sit, amet consectetur adipisicing elit.</p>
      <div class="visual blue"></div>
    </div>
    <div class="card yellow">
      <h3>Title - Card 3</h3>
      <p contenteditable>Short Description.</p>
      <div class="visual green"></div>
    </div>
  </div>
    `}
	cssCode={`
  .ex8 .parent {
    height: auto;
    display: grid;
    grid-gap: 1rem;
    grid-template-columns: repeat(3, 1fr);
  }

  .ex8 .visual {
    height: 100px;
    width: 100%;
  }

  .ex8 .card {
    display: flex;
    flex-direction: column;
    padding: 1rem;
    justify-content: space-between;
  }

  .ex8 h3 {
    margin: 0
  }
  `}
/>

<!-- 9 -->
<SectionContainer
	title="09. Clamping My Style"
	subCode="clamp(<min>, <actual>, <max>)"
	ChromeColor="green"
	EdgeColor="green"
	FirefoxColor="green"
	SafariColor="green"
	exercise="ex9"
	htmlCode={`
    <div class="parent white">
    <div class="card purple">
      <h1>Title Here</h1>
      <div class="visual yellow"></div>
      <p>Descriptive Text. Lorem ipsum dolor sit, amet consectetur adipisicing elit. Sed est error repellat veritatis.</p>
    </div>
  </div>
    `}
	cssCode={`
    .ex9 .parent {
    display: grid;
    place-items: center;
  }

  .ex9 .card {
    width: clamp(23ch, 50%, 46ch);
    display: flex;
    flex-direction: column;
    padding: 1rem;
  }

  .ex9 .visual {
      height: 125px;
      width: 100%;
    }
  
  `}
/>

<!-- 10 -->
<SectionContainer
	title="10. Respect for Aspect"
	subCode="aspect-ratio: <width> / <height>"
	ChromeColor="green"
	EdgeColor="green"
	FirefoxColor="green"
	SafariColor="green"
	exercise="ex10"
	htmlCode={`
    <div class="parent white">
    <div class="card blue">
      <h1>Video Title</h1>
      <div class="visual green"></div>
      <p>Descriptive Text. This demo works in Chromium 84+.</p>
    </div>
  </div>
    `}
	cssCode={`
    
  .ex10 .parent {
    display: grid;
    place-items: center;
  }

  .ex10 .visual {
    aspect-ratio: 16 / 9;
  }

  .ex10 .card {
    width: 50%;
    display: flex;
    flex-direction: column;
    padding: 1rem;
  }
  
  `}
/>
