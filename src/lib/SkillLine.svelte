<script>
    export let skillName = "DEFAULT"
    export let skillLevel = 0

    function skillLevelText() {
        switch (skillLevel) {
            case 0:
                return "DEFAULT"
            case 1:
                return "Developing"
            case 2:
                return "Advanced"
            case 3:
                return "Expert"
            default:
                return "DEFAULT"
        }
    }
</script>

<div class="flex flex-row w-full gap-2 h-20 items-center justify-center">
    <div class="flex w-1/3 items-end">
        <p class="text-lg font-bold text-end w-full">{skillName}</p>
    </div>
    <div class="bg-white w-1 h-full">

    </div>
    <div class="flex w-2/3 items-center">
        <div class={`bg-white flex flex-row h-6 items-center truncate ${skillLevel === 1 ? "w-1/2" : ""} ${skillLevel === 2 ? "w-3/4" : ""} ${skillLevel === 3 ? "w-full" : ""}`}>
            <p class="pl-1 invert-0 text-md font-ligh mix-blend-difference overflow-ellipsis">{skillLevelText(skillLevel)}</p>
        </div>
    </div>
</div>