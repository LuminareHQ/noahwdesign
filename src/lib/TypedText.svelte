<script>
    import {onMount} from "svelte";

    export let hideCursorOnEnd = false
    export let hideCursorBeforeStart = false

    export let textToType = ""
    let shownText = ""

    export let showCursor = true

    let Cursor = hideCursorBeforeStart

    export let timePerChar = 100

    export let delayStart = 0



    onMount(() => {
        if (hideCursorBeforeStart) {
            showCursor = false
        }
        setTimeout(() => {
            for (let i = 0; i < textToType.length; i++) {
                setTimeout(() => {
                    shownText += textToType[i]
                }, i * timePerChar)
            }

            setTimeout(() => {
                setInterval(() => {
                    Cursor = !Cursor
                }, 500)
            }, textToType.length * timePerChar)
        }, delayStart)
    }, delayStart)
</script>

{#each shownText as letter}{letter}{/each}{#if showCursor}{Cursor ? "_" : ""}{/if}
