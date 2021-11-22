<script context="module">
  import userConfig from '../config.json';

  export function load() {
    return {
      props: {
        config: userConfig
      }
    };
  }
</script>

<script>
  import SocialIcons from '../components/SocialIcons.svelte';
  import Avatar from '../components/Avatar.svelte';
  import { onMount } from 'svelte';

  export let config;
  let isLoading = true;

  onMount(() => {
    const html = document.querySelector('html');
    html.setAttribute('data-theme', config.theme);
    isLoading = false;
  });
</script>

<svelte:head>
  <title>{config.name} | Bio-Link</title>
  <meta name="title" content={`${config.name} | Bio-Link`} />
  <meta name="description" content={`${config.description} | Bio-Link`} />

  <!-- Open Graph / Facebook -->
  <meta property="og:type" content="website" />
  <meta property="og:url" content={config.biolinkUrl} />
  <meta property="og:title" content={`${config.name} | Bio-Link`} />
  <meta
    property="og:description"
    content={`${config.description} | Bio-Link`}
  />
  <meta property="og:image" content="/prev.png" />

  <!-- Twitter -->
  <meta property="twitter:card" content="summary_large_image" />
  <meta property="twitter:url" content={config.biolinkUrl} />
  <meta property="twitter:title" content={`${config.description} | Bio-Link`} />
  <meta
    property="twitter:description"
    content={`${config.description} | Bio-Link`}
  />
  <meta property="twitter:image" content="/prev.png" />
</svelte:head>

{#if !isLoading}
  <main
    class="w-full min-h-screen max-w-3xl flex items-center mx-auto p-4 flex-col overflow-y-auto"
  >
    <section class="w-full flex items-center flex-col pt-9">
      <Avatar avartarUrl={config.avatarUrl} />
      <h1 class="text-2xl text-center text-base-content">{config.name}</h1>
      <p class="text-base-content text-center opacity-60 mt-2">
        {config.description}
      </p>
    </section>
    <section class="w-full flex items-center flex-col mt-9 gap-6">
      {#each config.links as { url, text }}
        <a href={url} class="btn btn-primary">{text}</a>
      {/each}
    </section>
    <section class="w-full flex items-center justify-center mt-9 gap-6">
      <ul
        class="menu px-3 shadow-lg bg-base-200 rounded-box horizontal overflow-x-auto"
      >
        {#each config.social as { icon, url }}
          <li>
            <SocialIcons {icon} {url} />
          </li>
        {/each}
      </ul>
    </section>
    <section>
      <p class="text-xs opacity-70 mt-6">
        <a href="https://github.com/luizfverissimo/bio-link" class="link link-accent">Bio-Link</a> – Made with ❤️ by
        <a href="https://github.com/luizfverissimo" class="link">LF Verissimo</a
        >
      </p>
    </section>
  </main>
{/if}
