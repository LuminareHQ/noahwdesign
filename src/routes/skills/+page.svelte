<script>
    import SkillLine from "$lib/SkillLine.svelte";
</script>


<div class="flex flex-col w-full h-full gap-4 p-3">
    <div class="flex flex-col items-center w-full h-full">
        <div class="flex flex-col w-full items-center border-b-4 pb-2">
            <h2 class="text-2xl font-bold">Languages & Frameworks</h2>
        </div>
        <SkillLine skillName="SvelteKit" skillLevel={3}/>
        <SkillLine skillName="TypeScript" skillLevel={3}/>
        <SkillLine skillName="HTML/CSS" skillLevel={3}/>
        <SkillLine skillName="SQL" skillLevel={2}/>
        <SkillLine skillName="Go" skillLevel={2}/>
        <SkillLine skillName="NextJS" skillLevel={2}/>
        <SkillLine skillName="Object Pascal" skillLevel={2}/>
        <SkillLine skillName="C#" skillLevel={2}/>
        <SkillLine skillName="Python" skillLevel={1}/>
    </div>
    <div class="flex flex-col items-center pb-4">
        <div class="flex flex-col w-full items-center border-b-4 pb-2">
            <h2 class="text-2xl font-bold">Additional Skills</h2>
        </div>
        <SkillLine skillName="Responsive Design" skillLevel={3}/>
        <SkillLine skillName="Database SQL & No-SQL" skillLevel={3}/>
        <SkillLine skillName="API Design" skillLevel={3}/>
        <SkillLine skillName="Azure Devops" skillLevel={2}/>
        <SkillLine skillName="Git VCS" skillLevel={2}/>
        <SkillLine skillName="AWS" skillLevel={2}/>
        <SkillLine skillName="GCP" skillLevel={2}/>
        <SkillLine skillName="Docker" skillLevel={1}/>
    </div>
</div>