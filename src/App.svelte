<script>
    let wantedJobTitle = "Enginner";
    let firstname = "Santhosh";
    let email = "Santhosh~gmail";
    let country = "India";
    let lastName = "Kumar";
    let phone = "1234567890";
    let city = "Chennai";
    let address = "Chennai";
    let postalCode = "600100";
    let nationality = "Indian";
    let dob = "1996-09-10";
</script>

<div class="container">
    <div class="left">
        <!-- Content for the left side -->

        <input type="text" id="wantedJobTitle" bind:value={wantedJobTitle} />
        <label for="wantedJobTitle">wantedJobTitle</label><br />
        <input type="text" id="firstname" bind:value={firstname} />
        <label for="firstname">firstname</label><br />
        <input type="text" id="email" bind:value={email} />
        <label for="email">email</label><br />
        <input type="text" id="country" bind:value={country} />
        <label for="country">country</label><br />
        <input type="text" id="lastName" bind:value={lastName} />
        <label for="lastName">lastName</label><br />
        <input type="text" id="phone" bind:value={phone} />
        <label for="phone">phone</label><br />
        <input type="text" id="city" bind:value={city} />
        <input type="text" id="address" bind:value={address} />
        <label for="address">address</label><br />
        <input type="text" id="postalCode" bind:value={postalCode} />
        <label for="postalCode">postalCode</label><br />
        <input type="text" id="nationality" bind:value={nationality} />
        <label for="nationality">nationality</label><br />
        <input type="text" id="dob" bind:value={dob} />
        <label for="dob">dob</label><br />
    </div>
    <div class="right">
        wantedJobTitle: {wantedJobTitle} <br />
        firstname: {firstname} <br />
        email: {email} <br />
        country: {country} <br />
        lastName: {lastName} <br />
        phone: {phone} <br />
        city: {city} <br />
        address: {address} <br />
        postalCode: {postalCode} <br />
        nationality: {nationality} <br />
        dob: {dob} <br />
    </div>
</div>

<div class="container">
    <header>
        <h1>{firstname} {lastName}</h1>
        <p>Your Profession</p>
        <div class="contact-info">
            <p><strong>Email:</strong> {email}</p>
            <p><strong>Phone:</strong> (123) 456-7890</p>
            <p><strong>Address:</strong> 123 Main Street, City, State, Zip</p>
        </div>
    </header>
    <main>
        <section>
            <h2>Summary</h2>
            <p>A brief summary about yourself and your professional goals.</p>
        </section>
        <section>
            <h2>Experience</h2>
            <div class="experience">
                <h3>Job Title</h3>
                <p>Company Name, Location</p>
                <p>Start Date - End Date</p>
                <ul>
                    <li>Job responsibility 1</li>
                    <li>Job responsibility 2</li>
                    <li>Job responsibility 3</li>
                </ul>
            </div>
            <!-- Add more experience sections as needed -->
        </section>
        <section>
            <h2>Education</h2>
            <div class="education">
                <h3>Degree or Certification</h3>
                <p>Institution Name, Location</p>
                <p>Graduation Year</p>
            </div>
            <!-- Add more education sections as needed -->
        </section>
        <section>
            <h2>Skills</h2>
            <ul>
                <li>Skill 1</li>
                <li>Skill 2</li>
                <li>Skill 3</li>
            </ul>
        </section>
    </main>
</div>

<style>
    /* Reset some default styles */
    body,
    h1,
    h2,
    h3,
    p,
    ul {
        margin: 0;
        padding: 0;
    }

    body {
        font-family: Arial, sans-serif;
        line-height: 1.5;
    }

    .container {
        max-width: 800px;
        margin: 0 auto;
        padding: 20px;
    }

    header {
        text-align: center;
        margin-bottom: 30px;
    }

    h1 {
        font-size: 36px;
        margin-bottom: 10px;
    }

    .contact-info {
        margin-top: 10px;
    }

    main {
        margin-bottom: 30px;
    }

    section {
        margin-bottom: 20px;
    }

    h2 {
        font-size: 24px;
        margin-bottom: 10px;
    }

    h3 {
        font-size: 18px;
        margin-bottom: 5px;
    }

    ul {
        list-style-type: disc;
        margin-left: 20px;
    }

    .experience,
    .education {
        margin-bottom: 15px;
    }
</style>
