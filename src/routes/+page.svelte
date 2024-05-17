<div class="p-3 flex flex-col w-full h-full gap-2">
    <div class="flex flex-row w-full justify-between items-end">
        <p class="font-bold">Current Venture</p>
        <a href="https://ossiaperformance.com" target="_blank" class="link">Go To Site</a>
    </div>
    <div class="flex flex-col w-full h-full relative">
        <!--Prevent Interaction with the Iframe-->
        <div class="top-0 right-0 bottom-0 left-0 z-10 absolute"></div>
        <iframe src="https://ossiaperformance.com" frameborder="1" style="visibility:hidden;" onload="this.style.visibility = 'visible';" class="flex w-full h-full bg-black"></iframe>
    </div>
</div>