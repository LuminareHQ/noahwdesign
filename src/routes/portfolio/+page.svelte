<script>
  import PortfolioItem from "$lib/PortfolioItem.svelte";
</script>

<div class="flex flex-col w-full gap-2 p-3">
  <PortfolioItem
    title="Ossia Performance Homepage"
    iframeSrc="https://ossiaperformance.com"
    imageSrc="/ossia-performance-homepage.png"
    useImage="true"
    link="https://ossiaperformance.com"
    technologies={["SvelteKit", "Cloudflare"]}
    index="0" />
  <PortfolioItem
    title="Ossia Performance WebApp"
    iframeSrc="https://app.ossiaperformance.com"
    imageSrc="/ossia-performance-app.png"
    link="https://app.ossiaperformance.com"
    technologies={[
      "SvelteKit",
      "Cloudflare",
      "AWS",
      "MariaDB",
      "Go",
      "Open Sheet Music Display",
      "PDFJS",
      "ViewerJS",
    ]}
    useImage="true"
    index="1" />
  <PortfolioItem
    title="Open Marching"
    iframeSrc="https://openmarching.org"
    imageSrc="/open-marching.png"
    link="https://openmarching.org"
    technologies={[
      "SvelteKit",
      "Cloudflare",
      "Godot",
      "Lua",
    ]}
    useImage={true}
    index="2" />
<!--  <PortfolioItem-->
<!--    title="MarchLink"-->
<!--    iframeSrc="https://development.marchlink.com"-->
<!--    imageSrc="/marchlink.png"-->
<!--    useImage="true"-->
<!--    link="https://development.marchlink.com"-->
<!--    technologies={["SvelteKit", "Cloudflare", "AWS", "PocketBase", "Go"]}-->
<!--    index="3" />-->
</div>
