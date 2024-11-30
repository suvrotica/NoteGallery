
<script>
    import { onMount } from 'svelte';
    import Gallery from "$lib/component/Gallery.svelte";

    let images = [];

    onMount(async () => {
        const res = await fetch('/api/images');
        images = await res.json();
    });
</script>

<Gallery/>
<h1>Welcome to SvelteKit</h1>
<p>Visit <a href="https://svelte.dev/docs/kit">svelte.dev/docs/kit</a> to read the documentation</p>