<script>
    import {page} from '$app/stores'

    const btn_classes = `btn join-item`
</script>

<div class="flex flex-row w-full items-center justify-center">
    <div class="join">
        <a href="/" class={btn_classes} class:btn-neutral={$page.url.pathname === "/"}>Home</a>
        <a href="/about" class={btn_classes} class:btn-neutral={$page.url.pathname === "/about"}>About</a>
        <a href="/portfolio" class={btn_classes} class:btn-neutral={$page.url.pathname === "/portfolio"}>Portfolio</a>
        <a href="/resume" class={btn_classes} class:btn-neutral={$page.url.pathname === "/resume"}>Resume</a>
    </div>
</div>