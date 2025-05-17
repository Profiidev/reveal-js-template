<script lang="ts">
  import { onMount } from 'svelte';
  import Presentation from './Presentation.svelte';
  import Reveal from 'reveal.js';
  import Markdown from 'reveal.js/plugin/markdown/markdown';
  import Highlight from 'reveal.js/plugin/highlight/highlight';
  import Notes from 'reveal.js/plugin/notes/notes';
  import ClipCode from '@edc4it/reveal.js-railroad';
  import { Tldreveal } from 'tldreveal';

  import 'reveal.js/dist/reveal.css';
  import 'reveal.js/dist/theme/black.css';
  import 'reveal.js/plugin/highlight/monokai.css';
  import 'tldreveal/dist/esm/index.css';

  onMount(() => {
    const deck = new Reveal({
      plugins: [Markdown, Highlight, Notes, ClipCode, Tldreveal],
      autoAnimateEasing: 'ease',
      autoAnimateDuration: 1,
      scrollActivationWidth: undefined,
      hash: true,
      dependencies: [
        {
          src: 'node_modules/revealjs-animated/dist/revealjs-animated.js',
          async: true
        }
      ]
    });
    deck.initialize();
    // @ts-ignore
    window.Reveal = deck;
  });
</script>

<div class="reveal">
  <div class="slides">
    <Presentation />
  </div>
</div>
