<script>
    import PortfolioItem from '$lib/PortfolioItem.svelte'
</script>
<div class="flex flex-col w-full overflow-auto gap-2 p-3">
    <PortfolioItem title="Ossia Performance Homepage" iframeSrc="https://ossiaperformance.com"
                   link="https://ossiaperformance.com" technologies={["SvelteKit","Cloudflare"]} index="0"/>
    <PortfolioItem title="Ossia Performance WebApp" iframeSrc="https://app.ossiaperformance.com"
                   link="https://app.ossiaperformance.com" technologies={["SvelteKit","Cloudflare","PocketBase"]} useImage="true"
                   index="1"/>
    <PortfolioItem title="MarchLink" iframeSrc="https://development.marchlink.com"
                   link="https://development.ossiaperformance.com" technologies={["SvelteKit","Cloudflare","PocketBase"]} index="2"/>
</div>