<script>
    let resume = {
        wantedJobTitle: { value: "Engineer", type: "text" },
        firstname: { value: "Santhosh", type: "text" },
        email: { value: "Santhosh@example.com", type: "email" },
        country: { value: "India", type: "text" },
        lastName: { value: "Kumar", type: "text" },
        phone: { value: "1234567890", type: "tel" },
        city: { value: "Chennai", type: "text" },
        address: { value: "Chennai", type: "text" },
        postalCode: { value: "600100", type: "text" },
        nationality: { value: "Indian", type: "text" },
        dob: { value: "1996-09-10", type: "date" },
    };

    let additionalProps = {
        cat: { value: "meow", type: "text" },
        dog: { value: "bark", type: "text" },
    };

    resume = { ...resume, ...additionalProps };
</script>

<div class="resume">
    <header>
        <h1>John Doe</h1>
        <p>Web Developer</p>
        <p>Email: john.doe@example.com | Phone: (123) 456-7890</p>
        <p>LinkedIn: linkedin.com/in/johndoe | GitHub: github.com/johndoe</p>
    </header>
    <section>
        <h2>Profile</h2>
        <p>
            Experienced web developer with a strong background in developing
            award-winning applications for a diverse clientele. Proven ability
            to deliver high-quality web solutions on time and within budget.
        </p>
    </section>
    <section>
        <h2>Experience</h2>
        <div class="job">
            <h3>Senior Web Developer</h3>
            <p>XYZ Company | Jan 2020 - Present</p>
            <ul>
                <li>
                    Lead a team of 10 developers to create dynamic and
                    responsive websites for clients.
                </li>
                <li>
                    Implemented new features and improved existing ones based on
                    client feedback.
                </li>
                <li>
                    Ensured cross-browser compatibility and optimized websites
                    for speed and scalability.
                </li>
            </ul>
        </div>
        <div class="job">
            <h3>Web Developer</h3>
            <p>ABC Corp | Jun 2015 - Dec 2019</p>
            <ul>
                <li>Developed and maintained multiple e-commerce websites.</li>
                <li>
                    Collaborated with designers to create intuitive and engaging
                    user interfaces.
                </li>
                <li>
                    Conducted A/B testing to enhance website performance and
                    user experience.
                </li>
            </ul>
        </div>
    </section>
    <section>
        <h2>Education</h2>
        <p>Bachelor of Science in Computer Science</p>
        <p>University of Somewhere, 2011 - 2015</p>
    </section>
    <section>
        <h2>Skills</h2>
        <ul class="skills">
            <li>HTML, CSS, JavaScript</li>
            <li>React, Angular, Vue.js</li>
            <li>Node.js, Express</li>
            <li>SQL, NoSQL</li>
            <li>Git, GitHub</li>
        </ul>
    </section>
    <section>
        <h2>Certifications</h2>
        <p>Certified Web Developer, ABC Institute</p>
    </section>
</div>

<style>
    body {
        font-family: Arial, sans-serif;
        line-height: 1.6;
        background-color: #f4f4f4;
        margin: 0;
        padding: 0;
    }

    .resume {
        max-width: 800px;
        margin: 2rem auto;
        padding: 2rem;
        background: #fff;
        box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
    }

    header {
        text-align: center;
        border-bottom: 2px solid #eee;
        margin-bottom: 2rem;
        padding-bottom: 1rem;
    }

    header h1 {
        margin: 0;
        font-size: 2.5rem;
        color: #333;
    }

    header p {
        margin: 0.5rem 0;
        color: #777;
    }

    section {
        margin-bottom: 1.5rem;
    }

    section h2 {
        font-size: 1.5rem;
        color: #333;
        border-bottom: 2px solid #eee;
        padding-bottom: 0.5rem;
        margin-bottom: 1rem;
    }

    .job h3 {
        margin: 0;
        font-size: 1.2rem;
        color: #333;
    }

    .job p {
        margin: 0.5rem 0;
        color: #777;
    }

    .job ul {
        list-style-type: disc;
        padding-left: 1.5rem;
    }

    .skills {
        display: flex;
        flex-wrap: wrap;
    }

    .skills li {
        flex: 1 1 45%;
        margin-bottom: 0.5rem;
    }
</style>
