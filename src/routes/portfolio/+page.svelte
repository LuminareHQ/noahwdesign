<script>
    import PortfolioItem from '$lib/PortfolioItem.svelte'
</script>
<div class="flex flex-col w-full gap-2 p-3">
    <PortfolioItem title="Ossia Performance Homepage" iframeSrc="https://ossiaperformance.com"
                   imageSrc="/ossia-performance-homepage.png" useImage="true"
                   link="https://ossiaperformance.com" technologies={["SvelteKit","Cloudflare"]} index="0"/>
    <PortfolioItem title="Ossia Performance WebApp" iframeSrc="https://app.ossiaperformance.com"
                   imageSrc="/ossia-performance-app.png"
                   link="https://app.ossiaperformance.com"
                   technologies={["SvelteKit","Cloudflare","AWS","PocketBase","Go","Open Sheet Music Display","PDFJS"]}
                   useImage="true"
                   index="1"/>
    <PortfolioItem title="MarchLink" iframeSrc="https://development.marchlink.com" imageSrc="/marchlink.png"
                   useImage="true"
                   link="https://development.ossiaperformance.com"
                   technologies={["SvelteKit","Cloudflare","AWS","PocketBase","Go"]} index="2"/>
</div>