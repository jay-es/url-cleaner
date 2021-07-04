<script lang="ts">
  const searchParams = new URLSearchParams(window.location.search)
  let url = searchParams.get('text') ?? ''

  $: href = url.replace(/[?#].*/, "")
</script>

<main>
  <h1>URL Cleaner</h1>
  <textarea bind:value={url}></textarea>
  <a {href} target="_blank">{href}</a>
</main>

<style>
  h1 {
    font-size: 1rem;
    text-align: center;
  }

  textarea {
    width: 99%;
    height: 5em;
  }
</style>
