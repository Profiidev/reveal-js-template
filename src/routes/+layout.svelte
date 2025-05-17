<script lang="ts">
  import '../app.css';
  import 'reveal.js/dist/reset.css';
  import 'reveal.js/dist/reveal.css';
  import 'reveal.js/dist/theme/black.css';
  import 'reveal.js/plugin/highlight/monokai.css';

  let { children } = $props();
</script>

{@render children()}
