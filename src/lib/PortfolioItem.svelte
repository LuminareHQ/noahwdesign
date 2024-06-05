<script>
    export let index = 0
    export let title = "NO TITLE SET"
    export let useImage = false
    export let imageSrc = "/ossia-performance-app.png"
    export let iframeSrc = "https://example.com"
    export let link = "https://example.com"
    export let technologies = []
</script>

<div class={`flex flex-col w-full mx-auto border-2 ${index % 2 === 0 ? "lg:flex-row" : "lg:flex-row-reverse"}`}>
    <div class="flex flex-col w-full lg:w-2/3 h-full">
        <a class="flex flex-col relative h-full overflow-hidden" href={link} target="_blank">
            {#if useImage}
                <img src={imageSrc} class="object-contain h-full">
            {:else}
                <!--Prevent Interaction with the Iframe-->
                <div class="top-0 right-0 bottom-0 left-0 z-10 absolute"></div>
                <iframe src={iframeSrc} frameborder="1" style="visibility:hidden;"
                        onload="this.style.visibility = 'visible';" class="flex h-full w-full bg-black"></iframe>
            {/if}
            <div class="absolute overflow-hidden top-2 hover:right-0 -right-24 transition-all p-3 pr-5 bg-base-100 group rounded-l-2xl flex flex-row gap-4 ">
                <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24">
                    <path fill="none" stroke="currentColor" stroke-linecap="round" stroke-linejoin="round"
                          stroke-width="2"
                          d="M15 3h6v6m-11 5L21 3m-3 10v6a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2V8a2 2 0 0 1 2-2h6"/>
                </svg>
                <p>Go To Site</p>
            </div>
        </a>
    </div>
    <div class="flex flex-col p-2 w-full lg:w-1/3 gap-2">
        <h2 class="text-2xl">{title}</h2>
        <p>Technologies Utilized:</p>
        <div class="flex flex-row flex-wrap gap-2">
            {#each technologies as technology}
                <div class="p-1 border-[1px]">{technology}</div>
            {/each}
        </div>
    </div>
</div>

<style>
</style>