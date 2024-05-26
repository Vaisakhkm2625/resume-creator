<script>
    import "@picocss/pico";
    import Template from "./Templates/Template.svelte";
    import Template1 from "./Templates/Template1.svelte";
    import Input from "./lib/Input.svelte";
    import ListView from "./lib/ListView.svelte";

    let templatePaths = "../Templates/*.svelte";
    let showReactiveVariables = false;

    let resume = {
        WantedJobTitle: { value: "Engineer", type: "text" },
        FirstName: { value: "Santhosh", type: "text" },
        Description: {
            value: "Santhosh@example.com",
            type: "textarea",
            class: "full-width",
        },
        Email: { value: "Santhosh@example.com", type: "email" },
        Country: { value: "India", type: "text" },
        LastName: { value: "Kumar", type: "text" },
        Phone: { value: "1234567890", type: "tel" },
        City: { value: "Chennai", type: "text" },
        Address: { value: "Chennai", type: "text" },
        PostalCode: { value: "600100", type: "text" },
        Nationality: { value: "Indian", type: "text" },
        DateOfBirth: { value: "1996-09-10", type: "date" },
    };

    function handleSubmit() {
        console.log("Form submitted with:", resume);
    }
</script>

<header class="container">
    <h1 class="">Resume Bulder</h1>
</header>
<main class="container">
    <div>
        <form on:submit|preventDefault={handleSubmit} class="custom-grid">
            {#each Object.entries(resume) as [key, field]}
                <Input bind:resume bind:key bind:field></Input>
                <!--<input type="text" id={key} bind:value={field.value} /> -->
            {/each}
            <button type="submit" class="full-width">Submit</button>
        </form>
    </div>

    <div class="template-container">
        <Template1 bind:resume />
    </div>

    <div class="picker grid">
        <Template bind:resume />
        <Template bind:resume />
        <Template1 bind:resume />
        <Template1 bind:resume />
        <Template1 bind:resume />
        <Template1 bind:resume />
    </div>
    <ListView />

    <div>
        {#if showReactiveVariables}
            <div>
                wantedJobTitle: {resume.WantedJobTitle.value} <br />
                firstname: {resume.FirstName.value} <br />
                email: {resume.Email.value} <br />
                country: {resume.Country.value} <br />
                lastName: {resume.LastName.value} <br />
                phone: {resume.Phone.value} <br />
                city: {resume.City.value} <br />
                address: {resume.Address.value} <br />
                postalCode: {resume.PostalCode.value} <br />
                nationality: {resume.Nationality.value} <br />
                dob: {resume.DateOfBirth.value} <br />
            </div>
        {/if}
    </div>
</main>

<style>
    /*form {
        display: grid;
        grid-template-columns: 1fr 1fr;
        gap: 1rem;
    }*/
    :global(.full-width) {
        grid-column: span 2;
    }
    .template-container {
        border: 1px solid black;
    }
    .picker {
        zoom: 0.4;
        -moz-transform: scale(3);
        -moz-transform-origin: 0 0;
    }

    .custom-grid {
        display: grid;
        grid-template-columns: 1fr 1fr;
        grid-column-gap: 20px;
        grid-row-gap: 20px;
        justify-items: stretch;
        align-items: stretch;
    }
</style>
