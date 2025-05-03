<script>
    import ResumeItem from "$lib/ResumeItem.svelte";
</script>

<div class="p-3 flex flex-col w-full h-full gap-4">
    <div class="flex flex-col w-full">
        <p>Developer with an Artists Touch.</p>
    </div>
    <div class="flex flex-col w-full gap-4">
        <h2 class="text-3xl font-bold">Experience</h2>
        <ResumeItem
                header="SigmaNEST (Formerly Cambrio)"
                location="Cincinnati, Ohio"
                title="Post Developer"
                dates="April 2023 - PRESENT"
                description={`Leveraged expertise in Object Pascal and a custom PST language to develop "Post Translation Programs" for SigmaNEST. These programs automate NC code conversion, improving machine compatibility and streamlining the manufacturing process.`}/>
        <ResumeItem
                header="Cambrio"
                location="Cincinnati, Ohio"
                title="Applications Engineer"
                dates="September 2022 - April 2023"
                description="Provided technical assistance to customers using the SigmaNEST suite of software, and developed internal tools that reduced redundant tasks and increased team efficiency and collaboration."/>
    </div>
    <div class="flex flex-col w-full gap-4">
        <h2 class="text-3xl font-bold">Education</h2>
        <ResumeItem
                header="University of Kentucky"
                location="Lexington, KY"
                title="Digital Media and Design"
                dates="August 2018 - May 2022"
                description="Bachelor of Science in Digital Media and Design with a focus on Interactive Development (Web, Desktop, VR/Game Development)"/>
    </div>
    <div class="flex flex-col w-full gap-4">
        <h2 class="text-3xl font-bold">Projects</h2>
        <ResumeItem
                header="SigmaSidekick"
                location="SigmaNEST Internal Tooling"
                title="Lead Developer"
                dates=""
                description="Developed an internal suite of software tools using Tauri, to assist the Operations Department with their everyday tasks."/>
        <ResumeItem
                header="Ossia Performance"
                location="Music Technology Startup"
                title="Co-Founder, Lead Developer"
                dates=""
                description="Music Technology Web-based startup for performing arts groups, utilizing SvelteKit, PostgreSQL, Redis, various AWS services, hosted on Railway."/>
        <ResumeItem
                header="DotFlow"
                location="Open-Source Marching Drill Software"
                title="Lead Developer"
                dates=""
                description="Developing an open source marching drill software, utilizing SQLite, Svelte, ThreeJS, Tauri, and Python for scripting."/>
    </div>
    <div class="flex flex-col w-full gap-4">
        <h2 class="text-3xl font-bold">Languages</h2>
        <ul class="list-disc list-inside">
            <li>SvelteKit</li>
            <li>TypeScript</li>
            <li>Python</li>
            <li>HTML/CSS</li>
            <li>SQL</li>
            <li>Rust</li>
            <li>Go</li>
            <li>C#</li>
            <li>Object Pascal</li>
        </ul>
    </div>
    <div class="flex flex-col w-full gap-4">
        <h2 class="text-3xl font-bold">Skills</h2>
        <ul class="list-disc list-inside">
            <li>Cross-Browser Compatible, Responsive, and ARIA Compliant Design</li>
            <li>SQL & No-SQL Database Administration</li>
            <li>Azure DevOps & Git VCS</li>
            <li>API Design & Integration</li>
            <li>Scalable full-stack infrastructure and Containerization</li>
        </ul>
    </div>
    <div class="flex flex-col w-full gap-4 max-w-2xl">
        <h2 class="text-3xl font-bold">Achievements</h2>
        <ResumeItem
                hideComma="true"
                header="SigmaSidekick"
                location=""
                title="SigmaNEST Internal Tooling"
                dates=""
                description="Developed a tool within the SigmaSidekick desktop app that reads in a supplier’s machine parameter PDF file, analyzes and parses out relevant information, and formats it into a SigmaNEST Tech Table from user defined options, reducing a manual multiday process, to around 30 seconds."/>
    </div>
    <div class="py-12">
        <a href="/Weber_Noah_Resume_Public.pdf" class="border-2 p-2" download
        >Download A Copy</a>
    </div>
</div>
