<div class="p-3 flex flex-col w-full h-full gap-2">
    <div class="flex flex-row w-full justify-between items-end">
        <p class="font-bold">Current Venture</p>
    </div>

    <div class="flex flex-col w-full h-full relative overflow-hidden">
        <!--Prevent Interaction with the Iframe-->
        <a href="https://ossiaperformance.com" target="_blank" class="flex flex-col w-full h-full relative overflow-hidden ">
            <img src="/ossia-performance-homepage.png" alt="" class="flex w-full h-full object-cover lg:opacity-0 opacity-100 transition-opacity absolute top-0 bottom-0 right-0 left-0">
            <div class="absolute overflow-hidden top-2 hover:right-0 -right-24 transition-all p-3 pr-5 bg-base-100 group rounded-l-2xl flex flex-row gap-4 z-20">
                <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24">
                    <path fill="none" stroke="currentColor" stroke-linecap="round" stroke-linejoin="round"
                          stroke-width="2"
                          d="M15 3h6v6m-11 5L21 3m-3 10v6a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2V8a2 2 0 0 1 2-2h6"/>
                </svg>
                <p class="text-white">Go To Site</p>
            </div>
            <div class="flex w-full h-full relative max-lg:opacity-0 opacity-100 transition-opacity">
                <div class="top-0 right-0 bottom-0 left-0 -z-10 absolute max-lg:opacity-0 opacity-100 transition-opacity"></div>
                <div class="max-lg:opacity-0 opacity-100 transition-opacity flex w-full h-full -z-50">
                    <iframe src="https://ossiaperformance.com" frameborder="1" style="visibility:hidden;"
                            onload="this.style.visibility = 'visible';" class="flex w-full h-full bg-black -z-20"></iframe>
                </div>
            </div>
        </a>
    </div>
</div>