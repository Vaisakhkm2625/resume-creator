<script>
    // Import the components dynamically using Vite's import.meta.glob
    const modules = import.meta.glob("../Templates/*.svelte");

    // Convert the modules object into an array of promises
    let components = [];

    // Load all components dynamically
    for (const path in modules) {
        modules[path]().then((module) => {
            components = [...components, module.default];
        });
    }
</script>

<div class="grid picker">
    {#if components.length > 0}
        {#each components as Component}
            <Component />
        {/each}
    {:else}
        <p>Loading components...</p>
    {/if}
</div>

<style>
    .picker {
        zoom: 0.4;
        -moz-transform: scale(3);
        -moz-transform-origin: 0 0;
    }
</style>
