<!-- App.svelte -->
<script>
    let title = "Shashidhar S A";
    let contactInfo = {
        email: "shashidharsa32@gmail.com",
        mobile: "8217891984"
    };
    let experience = [
        {
            title: "Manager Impact - Magic Bus India Foundation (June 23 - Present)",
            details: [
                "Led the M&E for the integration of life skills into the curriculum across 1300 government schools...",
                "Developed and operationalized a comprehensive M&E framework...",
                // Other experience details
            ]
        },
        // Other experience items
    ];
    let education = "Siddaganga Institute of Technology, Bengaluru India (2012-2016) - Tech & Engineering Science Mathematics.";
    let additionalInfo = {
        summary: "In short summary: Working, learning, and experienced across 5 states with various roles...",
        languages: ["Kannada", "English", "Hindi", "Telugu"],
        learning: "Currently learning Japanese.",
        monitoringEval: "[Link]",
        linkedin: "https://www.linkedin.com/in/shashidhar-sa-535778b1/"
    };
    let footerText = "&copy; 2024 Shashidhar S A";
</script>

<header>
    <h1>{title}</h1>
</header>

<div class="container">
    <div class="section-content contact-info">
        <p>Email: {contactInfo.email}</p>
        <p>Mobile: {contactInfo.mobile}</p>
    </div>

    <div class="section">
        <div class="section-title">Experience</div>
        {#each experience as exp}
            <div class="section-content">
                <div class="job-title">{exp.title}</div>
                <ul>
                    {#each exp.details as detail}
                        <li>{detail}</li>
                    {/each}
                </ul>
            </div>
        {/each}
    </div>

    <div class="section">
        <div class="section-title">Education and Qualifications</div>
        <div class="section-content">
            <p>{education}</p>
        </div>
    </div>

    <div class="section">
        <div class="section-title">Additional Information</div>
        <div class="section-content">
            <p>{additionalInfo.summary}</p>
            <p>Known Languages: {additionalInfo.languages.join(", ")}</p>
            <p>{additionalInfo.learning}</p>
            <p>Monitoring evaluation & Data Profile: <a href={additionalInfo.monitoringEval} target="_blank">{additionalInfo.monitoringEval}</a></p>
            <p>LinkedIn profile: <a href={additionalInfo.linkedin} target="_blank">{additionalInfo.linkedin}</a></p>
        </div>
    </div>

    <footer>
        <p>{footerText}</p>
    </footer>
</div>
