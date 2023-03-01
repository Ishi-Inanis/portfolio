<script>
  import H2 from './H2.svelte';

  export let title;
</script>

<article
    class="space-y-4 p-6 bg-neutral-200/40 dark:bg-neutral-800/40 border border-neutral-50 dark:border-neutral-700 rounded-xl backdrop-blur-lg">
  <H2>{title}</H2>
  <slot/>
</article>