<script>
    export let header = ""
    export let location = ""
    export let title = ""
    export let dates = ""
    export let description = ""
    export let hideComma = false
</script>

<div class="flex flex-col w-full gap-1">
    <p class="text-lg"><span class="font-bold">{header}{#if !hideComma},{/if}</span>
        {location} - <span class="italic">{title}</span>
    </p>
    <p class="text-xs opacity-80">{dates}</p>
    <p class="max-w-2xl">{description}</p>
</div>