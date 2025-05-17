<script lang="ts">
  import Code from './Code.svelte';
  import Markdown from './Markdown.svelte';
  import Notes from './Notes.svelte';
  import Slide from './Slide.svelte';
</script>

<Slide>
  <p class="capitalize">Svelte deck 🔥</p>
</Slide>

<Slide>
  <p class="capitalize">With Notes</p>
  <Notes>
    <p>These are notes</p>
    <p>They are not visible in the presentation</p>
  </Notes>
</Slide>

<Slide>
  <p class="capitalize">Horizontal slide</p>
</Slide>

<Slide>
  <Slide>
    <p class="capitalize">Vertical slide 1</p>
  </Slide>
  <Slide>
    <p class="capitalize">Vertical slide 2</p>
  </Slide>
</Slide>

<Slide id="animate" animate>
  <p class="capitalize">Animate elements</p>
</Slide>

<Slide id="animate" animate>
  <p class="capitalize">Animate elements</p>
  <p class="capitalize">Across slides</p>
</Slide>

<Slide id="list" animate>
  <ul>
    <li>React</li>
    <li>Solid</li>
    <li>Svelte</li>
    <li>Vue</li>
  </ul>
</Slide>

<Slide id="list" animate>
  <ul>
    <li>Svelte</li>
    <li>React</li>
    <li>Solid</li>
    <li>Vue</li>
  </ul>
</Slide>

<Slide id="list" animate>
  <ul>
    <li>Svelte ❤️</li>
    <li>React</li>
    <li>Solid</li>
    <li>Vue</li>
  </ul>
</Slide>

<Slide>
  <p class="capitalize">Code Blocks</p>
</Slide>

<Slide animate>
  <Code id="code" lines="1|3">
    {`
			<Slide animate>
				<!-- .. -->
			</Slide>
		`}
  </Code>
</Slide>

<Slide animate>
  <Code id="code" lines="2|4">
    {`
			<Slide animate>
				<Code lines>
					<!-- ... -->
				</Code>
			</Slide>
		`}
  </Code>
</Slide>

<Slide animate>
  <Code id="code" lines="3-5|1-7">
    {`
			<Slide animate>
				<Code lines>
					{code\`
						...
					\`}
				</Code>
			</Slide>
		`}
  </Code>
</Slide>

<Slide id="boxes" animate>
  <p class="capitalize">Cool transitions</p>
  <div class="flex place-content-center gap-2">
    <div data-id="box-1" class="h-[100px] w-[100px] bg-gray-400"></div>
    <div data-id="box-2" class="h-[100px] w-[100px] bg-gray-400"></div>
    <div data-id="box-3" class="h-[100px] w-[100px] bg-gray-400"></div>
  </div>
</Slide>

<Slide id="boxes" animate>
  <p class="capitalize">Moving boxes</p>
  <div class="flex place-content-center gap-2">
    <div data-id="box-1" class="h-[200px] w-[200px] bg-red-400"></div>
    <div data-id="box-2" class="h-[200px] w-[200px] bg-green-400"></div>
    <div data-id="box-3" class="h-[200px] w-[200px] bg-blue-400"></div>
  </div>
  <p class="capitalize">Cool transitions</p>
</Slide>

<Slide id="boxes" animate>
  <p>Moving boxes</p>
  <div class="flex place-content-center gap-2">
    <div data-id="box-1" class="h-[200px] w-[200px] bg-gray-400"></div>
    <img
      src="https://i.giphy.com/media/ToMjGpnXBTw7vnokxhu/giphy.webp"
      alt="Whoa"
    />
    <div data-id="box-3" class="h-[200px] w-[200px] bg-gray-400"></div>
  </div>
  <p>Whoa!</p>
</Slide>

<Markdown>
  {`
		## Markdown ❤️
		You can use **HTML** or **Markdown** for slides.
	`}
</Markdown>

<Markdown name="example.md" external />

<Slide>
  <p class="capitalize">Get started 😎</p>
</Slide>
