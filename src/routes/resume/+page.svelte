<script>
    import ResumeItem from "$lib/ResumeItem.svelte";
</script>

<div class="p-3 flex flex-col w-full h-full gap-4">
    <div class="flex flex-col w-full">
        <p>I bridge the gap between creativity and capability.</p>
        <p>Building platforms users want, with the functionality they need.</p>
    </div>
    <div class="flex flex-col w-full gap-4">
        <h2 class="text-2xl font-bold">Experience</h2>
        <ResumeItem
                header="Cambrio"
                location="Cincinnati, Ohio"
                title="Post Developer"
                dates="April 2023 - PRESENT"
                description={`Leveraged expertise in Object Pascal and a custom PST language to develop "Post Translation Programs" for SigmaNEST. These programs automate NC code conversion, improving machine compatibility and streamlining the manufacturing process.`}/>
        <ResumeItem
                header="Cambrio"
                location="Cincinnati, Ohio"
                title="Applications Engineer"
                dates="September 2022 - April 2023"
                description="Provided technical assistance to customers utilizing the SigmaNEST suite of software tools, and developed internal tools that refined team workflows and increased team efficiency and collaboration."/>
    </div>
    <div class="flex flex-col w-full gap-4">
        <h2 class="text-2xl font-bold">Education</h2>
        <ResumeItem
                header="University of Kentucky"
                location="Lexington, KY"
                title="Digital Media and Design"
                dates="August 2018 - May 2022"
                description="Bachelor of Science in Digital Media and Design with a focus on Interactive Development (Web, Desktop, VR/Game Development)"/>
    </div>
    <div class="flex flex-col w-full gap-4">
        <h2 class="text-2xl font-bold">Projects</h2>
        <ResumeItem
                hideComma="true"
                header="Ossia Performance"
                location=""
                title="Co-Founder, Lead Developer"
                dates="February 2024 - Present"
                description="Music Technology Startup using SvelteKit, Node.js, MariaDB, and Stripe on AWS and Cloudflare cloud infrastructure."/>
        <ResumeItem
                hideComma="true"
                header="Open Marching"
                location=""
                title="Founder"
                dates=""
                description="Developing open source software for the marching arts, including an open source drill writing/ visualization software bundle called DotFlow."/>
    </div>
    <div class="flex flex-col w-full gap-4">
        <h2 class="text-2xl font-bold">Skills</h2>
        <ul class="list-disc list-inside">
            <li>Cross-Browser Compatible, Responsive, and ARIA Compliant Design</li>
            <li>Database Administration</li>
            <li>Azure DevOps & Git VCS</li>
            <li>API Design & Integration</li>
            <li>Scalable full-stack infrastructure and Containerization</li>
        </ul>
    </div>
    <div class="flex flex-col w-full gap-4">
        <h2 class="text-2xl font-bold">Languages</h2>
        <ul class="list-disc list-inside">
            <li>SvelteKit</li>
            <li>TypeScript</li>
            <li>HTML/CSS</li>
            <li>Python</li>
            <li>Go</li>
            <li>SQL</li>
            <li>C#</li>
            <li>Object Pascal</li>
        </ul>
    </div>
    <div class="flex flex-col w-full gap-4 max-w-2xl">
        <h2 class="text-2xl font-bold">Achievements</h2>
        <ul class="list-disc list-inside">
            <li>
                Fast-tracked to Post Developer in 6 months by exceeding expectations. Developed internal tools that
                improved efficiency and cohesion throughout departments.
            </li>
            <li>
                Collaboratively contributed the second-highest number of posts (27 out of 121 YTD), driving a record
                number of deliveries in Q1, Q2, and Q3 in 2024.
            </li>
        </ul>
    </div>
    <div class="py-12">
        <a href="/Weber_Noah_Resume_Public.pdf" class="border-2 p-2" download
        >Download A Copy</a>
    </div>
</div>
