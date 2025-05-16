<script lang="ts">
  import type { Snippet } from 'svelte';

  interface Props {
    name?: string;
    external?: boolean;
    children?: Snippet;
  }

  let { name = 'example.md', external = false, children }: Props = $props();
</script>

{#if external}
  <section data-markdown={name}></section>
{:else}
  <section data-markdown>
    <div data-template>
      {@render children?.()}
    </div>
  </section>
{/if}
