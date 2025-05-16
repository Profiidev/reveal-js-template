<script lang="ts">
  import type { Snippet } from 'svelte';

  interface Props {
    id?: string;
    animate?: boolean;
    restart?: boolean;
    children?: Snippet;
  }

  let { id, animate = false, restart = false, children }: Props = $props();
</script>

<section
  data-auto-animate-id={id}
  data-auto-animate={animate || null}
  data-auto-animate-restart={restart || null}
>
  {@render children?.()}
</section>
