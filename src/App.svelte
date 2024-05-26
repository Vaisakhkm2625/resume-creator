<script>
    import "@picocss/pico";
    import Template from "./Templates/Template.svelte";
    import Template1 from "./Templates/Template1.svelte";
    import Input from "./lib/Input.svelte";
    let templatePaths = "../Templates/*.svelte";

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

    let showReactiveVariables = true;
    function handleSubmit() {
        console.log("Form submitted with:", resume);
    }
</script>

<main class="container">
    <div>
        <h1>Resume Bulder</h1>
        <form on:submit|preventDefault={handleSubmit} class="custom-grid">
            {#each Object.entries(resume) as [key, field]}
                <Inputa bind:resume bind:key bind:field></Inputa>
                <!--<input type="text" id={key} bind:value={field.value} /> -->
            {/each}
            <button type="submit" class="full-width">Submit</button>
        </form>
    </div>

    <Template1 bind:resume />

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

    .custom-grid {
        display: grid;
        grid-template-columns: 1fr 1fr;
        grid-column-gap: 20px;
        grid-row-gap: 20px;
        justify-items: stretch;
        align-items: stretch;
    }
</style>
