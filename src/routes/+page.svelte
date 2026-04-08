<script>
    console.log("hello world")
    import CanvasSquare from "$lib/components/CanvasSquare.svelte";
    import ClicksCounter from "$lib/components/ClicksCounter.svelte";
    let count = $state(5)
</script>

<h1>Welcome to SvelteKit</h1>
<p>Visit <a href="https://svelte.dev/docs/kit">svelte.dev/docs/kit</a> to read the documentation</p>

<ClicksCounter bind:initialCount={count} />
<p>Count from parent is {count}</p>
<ClicksCounter initialCount={3} />

<CanvasSquare />

<style>
    h1 {
    color: deepskyblue;
  }
</style>