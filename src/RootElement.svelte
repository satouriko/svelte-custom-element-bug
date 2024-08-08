<svelte:options
  customElement={{
    tag: 'root-custom-element',
    props: {},
  }}
/>

<script lang='ts'>
  function setMyElementVal() {
    ($host().querySelector('my-custom-element') as any).value = 'hello world'
  }
</script>

<slot />
<button onclick={() => setMyElementVal()}>click me</button>

<style>
  :host {
    display: block;
  }
</style>
