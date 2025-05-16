<script lang="ts">
  import type { Snippet } from 'svelte';

  interface Props {
    id?: string;
    lines?: string | boolean;
    noesacape?: boolean;
    children?: Snippet;
  }

  let { id, lines, noesacape = false, children }: Props = $props();
</script>

<pre data-id={id || null}>
  <code
    data-trim
    data-line-numbers={lines || null}
    data-noescape={noesacape || null}>
    {@render children?.()}
  </code>
</pre>
