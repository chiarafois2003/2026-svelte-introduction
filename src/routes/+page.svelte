<script>
    console.log("hello world")
    import { website } from "$lib/state.svelte.js";
    import CanvasSquare from "$lib/components/CanvasSquare.svelte";
    import ClicksCounter from "$lib/components/ClicksCounter.svelte";
    import TitleEditor from "$lib/components/TitleEditor.svelte";
    import TodoList from "$lib/components/TodoList.svelte";
    let count = $state(5)
</script>

<h1>{ website.title }</h1>
<p>Visit <a href="https://svelte.dev/docs/kit">svelte.dev/docs/kit</a> to read the documentation</p>

<TitleEditor />

<ClicksCounter bind:initialCount={count} />
  {#if count > 10 && count < 20}
    <p>Count from parent is {count}</p>
  {:else if count > 30}
    <p>That's a lot of click</p>
  {:else}  
    <p>Count is not in range</p>
  {/if}
<ClicksCounter initialCount={3} />

<CanvasSquare />

<TodoList />

<style>
    h1 {
    color: deepskyblue;
  }
</style>