<script lang="ts">
  document.addEventListener('click', (e) => {
    console.log('document', e, e.currentTarget);
  })
  document.getElementById('app')?.addEventListener('click', (e) => {
    console.log('#app', e, e.currentTarget);
  })
  function onclick(event: Event) {}
</script>

<svelte:options
  customElement={{
    tag: 'my-custom-element',
  }}
/>

<!-- svelte-ignore a11y_click_events_have_key_events -->
<!-- svelte-ignore a11y_no_static_element_interactions -->
<div {onclick}>
  <slot />
</div>
