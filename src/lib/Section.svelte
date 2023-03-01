<script>
  import H1 from './H1.svelte';

  export let title = '';
</script>

<section
    class="sm:max-w-screen-sm md:max-w-screen-md lg:max-w-screen-lg xl:max-w-screen-xl info-section">
  <H1>{title}</H1>
  <slot></slot>
</section>