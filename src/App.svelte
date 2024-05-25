<script>
    import "@picocss/pico";
    import Template from "./lib/Template.svelte";
    import Input from "./lib/Input.svelte";

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

    let showReactiveVariables = false;
    function handleSubmit() {
        console.log("Form submitted with:", resume);
    }
</script>

<main class="container">
    <div>
        <h1>INPUT</h1>
        <form on:submit|preventDefault={handleSubmit} class="custom-grid">
            {#each Object.entries(resume) as [key, field]}
                <Input {key} {field}></Input>
            {/each}
            <button type="submit" class="full-width">Submit</button>
        </form>
    </div>

    <Template bind:resume />

    <div>
        {#if showReactiveVariables}
            <div>
                wantedJobTitle: {resume.wantedJobTitle.value} <br />
                firstname: {resume.firstname.value} <br />
                email: {resume.email.value} <br />
                country: {resume.country.value} <br />
                lastName: {resume.lastName.value} <br />
                phone: {resume.phone.value} <br />
                city: {resume.city.value} <br />
                address: {resume.address.value} <br />
                postalCode: {resume.postalCode.value} <br />
                nationality: {resume.nationality.value} <br />
                dob: {resume.dob.value} <br />
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
