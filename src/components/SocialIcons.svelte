<script>
  import Fa from 'svelte-fa/src/fa.svelte';
  import * as FaIcon from '@fortawesome/free-brands-svg-icons';

  export let icon;
  export let url;
</script>

<a href={url} class="text-2xl text-base-content">
  {#if icon}
    <Fa icon={FaIcon[icon]} />
  {/if}
</a>
