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
        <div class="flex flex-col relative h-full aspect-video">
            {#if useImage}
                <img src={imageSrc} class="object-contain h-full">
            {:else}
                <!--Prevent Interaction with the Iframe-->
                <div class="top-0 right-0 bottom-0 left-0 z-10 absolute"></div>
                <iframe src={iframeSrc} frameborder="1" style="visibility:hidden;"
                        onload="this.style.visibility = 'visible';" class="flex h-full w-full bg-black"></iframe>
            {/if}
        </div>
    </div>
    <div class="flex flex-col p-2 w-full lg:w-1/3 gap-2">
        <h2 class="text-2xl">{title}</h2>
        <a href={link}>Link</a>
        <div class="flex flex-row flex-wrap gap-2">
            {#each technologies as technology}
                <div class="p-1 border-2">{technology}</div>
            {/each}
        </div>
    </div>
</div>

<style>
</style>