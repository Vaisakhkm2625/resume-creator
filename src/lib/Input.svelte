<script>
    export let key;
    export let field;
</script>

<div class={field.class}>
    <label for={key}
        >{key
            .replace(/([A-Z]+)/g, " $1")
            .replace(/([A-Z][a-z])/g, " $1")}</label
    >

    <!-- <input -->
    <!--     type={key.type} -->
    <!--     id={key} -->
    <!--     bind:value={resume[key].value} -->
    <!-- /> -->

    {#if field.type === "text"}
        <input type="text" id={key} bind:value={field.value} />
    {:else if field.type === "textarea"}
        <textarea id={key} bind:value={field.value}></textarea>
    {:else if field.type === "email"}
        <input type="email" id={key} bind:value={field.value} />
    {:else if field.type === "tel"}
        <input type="tel" id={key} bind:value={field.value} />
    {:else if field.type === "date"}
        <input type="date" id={key} bind:value={field.value} />
    {/if}
</div>
