<script>
  import "../app.postcss";
  import { onMount } from "svelte";
  import TypedText from "$lib/TypedText.svelte";
  import { goto } from "$app/navigation";
  import { page } from "$app/stores";

  export let data;

  let loading = true;
  let showSlot = false;

  onMount(() => {
    loading = false;
    addEventListener("keydown", (e) => {
      switch (e.key) {
        case "1":
          goto("/");
          break;
        case "2":
          goto("/skills");
          break;
        case "3":
          goto("/resume");
          break;
        case "4":
          goto("/portfolio");
          break;
      }
    });

    setTimeout(() => {
      showSlot = true;
    }, 2600);
  });

  let shiftPressed = false;

  let userInput = "";
</script>

<div class="flex w-full h-full p-4">
  <div class="flex flex-col border-2 w-full h-full justify-between">
    <div class="flex flex-col w-full p-4">
      <div class="flex flex-row w-full justify-between items-start h-8">
        <h1 class="text-2xl text-left justify-start">
          <TypedText
            textToType="NoahW.Design"
            showCursor={true}
            additionalText={userInput}
            timePerChar="100" />
        </h1>
        <div class="flex flex-row gap-2 overflow-hidden p-1">
          <a
            class="hover:-translate-y-1 transition-all"
            target="_blank"
            id="link-one"
            href="https://github.com/LuminareHQ">
            <svg
              xmlns="http://www.w3.org/2000/svg"
              width="24"
              height="24"
              viewBox="0 0 1536 1536">
              <path
                fill="currentColor"
                d="M519 1072q4-6-3-13q-9-7-14-2q-4 6 3 13q9 7 14 2m-28-41q-5-7-12-4q-6 4 0 12q7 8 12 5q6-4 0-13m-41-40q2-4-5-8q-7-2-8 2q-3 5 4 8q8 2 9-2m21 23q2-1 1.5-4.5t-3.5-5.5q-6-7-10-3t1 11q6 6 11 2m86 75q2-7-9-11q-9-3-13 4q-2 7 9 11q9 3 13-4m42 3q0-8-12-8q-10 0-10 8t11 8t11-8m39-7q-2-7-13-5t-9 9q2 8 12 6t10-10m642-317q0-212-150-362T768 256T406 406T256 768q0 167 98 300.5T606 1254q18 3 26.5-5t8.5-20q0-52-1-95q-6 1-15.5 2.5t-35.5 2t-48-4t-43.5-20T468 1073q-23-59-57-74q-2-1-4.5-3.5l-8-8l-7-9.5l4-7.5L415 967q6 0 15 2t30 15.5t33 35.5q16 28 37.5 42t43.5 14t38-3.5t30-9.5q7-47 33-69q-49-6-86-18.5t-73-39t-55.5-76T441 741q0-79 53-137q-24-62 5-136q19-6 54.5 7.5T614 505l26 16q58-17 128-17t128 17q11-7 28.5-18t55.5-26t57-9q29 74 5 136q53 58 53 137q0 57-14 100.5t-35.5 70T992 956t-62.5 26t-68.5 12q35 31 35 95q0 40-.5 89t-.5 51q0 12 8.5 20t26.5 5q154-52 252-185.5t98-300.5m256-480v960q0 119-84.5 203.5T1248 1536H288q-119 0-203.5-84.5T0 1248V288Q0 169 84.5 84.5T288 0h960q119 0 203.5 84.5T1536 288" />
            </svg>
          </a>
          <a
            class="hover:-translate-y-1 transition-all"
            target="_blank"
            id="link-two"
            href="https://linkedin.com/in/noah-weber-design">
            <svg
              xmlns="http://www.w3.org/2000/svg"
              width="24"
              height="24"
              viewBox="0 0 24 24">
              <path
                fill="currentColor"
                d="M20.447 20.452h-3.554v-5.569c0-1.328-.027-3.037-1.852-3.037c-1.853 0-2.136 1.445-2.136 2.939v5.667H9.351V9h3.414v1.561h.046c.477-.9 1.637-1.85 3.37-1.85c3.601 0 4.267 2.37 4.267 5.455v6.286zM5.337 7.433a2.06 2.06 0 0 1-2.063-2.065a2.064 2.064 0 1 1 2.063 2.065m1.782 13.019H3.555V9h3.564zM22.225 0H1.771C.792 0 0 .774 0 1.729v20.542C0 23.227.792 24 1.771 24h20.451C23.2 24 24 23.227 24 22.271V1.729C24 .774 23.2 0 22.222 0z" />
            </svg>
          </a>
          <a
            class="hover:-translate-y-1 transition-all"
            target="_blank"
            id="link-three"
            href="https://x.com/luminarehq">
            <svg
              xmlns="http://www.w3.org/2000/svg"
              width="24"
              height="24"
              viewBox="0 0 16 16">
              <path
                fill="currentColor"
                d="M9.294 6.928L14.357 1h-1.2L8.762 6.147L5.25 1H1.2l5.31 7.784L1.2 15h1.2l4.642-5.436L10.751 15h4.05zM7.651 8.852l-.538-.775L2.832 1.91h1.843l3.454 4.977l.538.775l4.491 6.47h-1.843z" />
            </svg>
          </a>
        </div>
      </div>
      <div class="flex flex-row flex-wrap w-full gap-x-4">
        <a
          href="/"
          class="h-6 hover:scale-105 transition-all w-[64px] whitespace-nowrap"
          class:font-bold={$page.url.pathname === "/"}>
          <TypedText
            textToType="1. Home"
            showCursor={true}
            hideCursorBeforeStart={true}
            hideCursorOnEnd={true}
            timePerChar="50"
            delayStart="500" />
        </a>
        <a
          href="/skills"
          class="h-6 hover:scale-105 transition-all w-[64px] whitespace-nowrap"
          class:font-bold={$page.url.pathname === "/skills"}>
          <TypedText
            textToType="2. Skills"
            showCursor={true}
            hideCursorBeforeStart={true}
            hideCursorOnEnd={true}
            timePerChar="50"
            delayStart="500" />
        </a>
        <a
          href="/resume"
          class="h-6 hover:scale-105 transition-all w-[75px] whitespace-nowrap"
          class:font-bold={$page.url.pathname === "/resume"}>
          <TypedText
            textToType="3. Resume"
            showCursor={true}
            hideCursorBeforeStart={true}
            hideCursorOnEnd={true}
            timePerChar="50"
            delayStart="500" />
        </a>
        <a
          href="/portfolio"
          class="h-6 hover:scale-105 transition-all w-[80px] whitespace-nowrap"
          class:font-bold={$page.url.pathname === "/portfolio"}>
          <TypedText
            textToType="4. Portfolio"
            showCursor={true}
            hideCursorBeforeStart={true}
            hideCursorOnEnd={true}
            timePerChar="50"
            delayStart="500" />
        </a>
      </div>
    </div>
    <div class="flex w-full h-full border-t-2 border-b-2 overflow-auto">
      <div class="flex w-full h-full relative" class:overflow-hidden={!showSlot}>
        {#if !showSlot}
          <div
            class="flex flex-col w-full h-full items-center justify-center absolute top-0 left-0 right-0 bottom-0 z-50 bg-base-100">
            <svg
              xmlns="http://www.w3.org/2000/svg"
              width="24"
              height="24"
              viewBox="0 0 24 24">
              <path
                fill="currentColor"
                d="M12,21L15.6,16.2C14.6,15.45 13.35,15 12,15C10.65,15 9.4,15.45 8.4,16.2L12,21"
                opacity="0">
                <animate
                  id="svgSpinnersWifi0"
                  fill="freeze"
                  attributeName="opacity"
                  begin="0;svgSpinnersWifi1.end+0.2s"
                  calcMode="discrete"
                  dur="0.25s"
                  values="0;1" />
                <animate
                  id="svgSpinnersWifi1"
                  fill="freeze"
                  attributeName="opacity"
                  begin="svgSpinnersWifi3.end+0.5s"
                  dur="0.001s"
                  values="1;0" />
              </path>
              <path
                fill="currentColor"
                d="M12,9C9.3,9 6.81,9.89 4.8,11.4L6.6,13.8C8.1,12.67 9.97,12 12,12C14.03,12 15.9,12.67 17.4,13.8L19.2,11.4C17.19,9.89 14.7,9 12,9Z"
                opacity="0">
                <animate
                  id="svgSpinnersWifi2"
                  fill="freeze"
                  attributeName="opacity"
                  begin="svgSpinnersWifi0.end"
                  calcMode="discrete"
                  dur="0.25s"
                  values="0;1" />
                <animate
                  fill="freeze"
                  attributeName="opacity"
                  begin="svgSpinnersWifi3.end+0.5s"
                  dur="0.001s"
                  values="1;0" />
              </path>
              <path
                fill="currentColor"
                d="M12,3C7.95,3 4.21,4.34 1.2,6.6L3,9C5.5,7.12 8.62,6 12,6C15.38,6 18.5,7.12 21,9L22.8,6.6C19.79,4.34 16.05,3 12,3"
                opacity="0">
                <animate
                  id="svgSpinnersWifi3"
                  fill="freeze"
                  attributeName="opacity"
                  begin="svgSpinnersWifi2.end"
                  calcMode="discrete"
                  dur="0.25s"
                  values="0;1" />
                <animate
                  fill="freeze"
                  attributeName="opacity"
                  begin="svgSpinnersWifi3.end+0.5s"
                  dur="0.001s"
                  values="1;0" />
              </path>
            </svg>
          </div>
        {/if}
        <slot />
      </div>
    </div>
    <div class="flex flex-row w-full p-4 truncate items-center">
      <p class="h-6 overflow-ellipsis">
        <TypedText
          textToType="© Copyright NoahW.Design 2023"
          showCursor={false}
          timePerChar="20"
          delayStart="2000" />
      </p>
    </div>
  </div>
  {#if loading}
    <div class="flex flex-col w-full h-full items-center justify-center">
      <svg
        xmlns="http://www.w3.org/2000/svg"
        width="24"
        height="24"
        viewBox="0 0 24 24">
        <path
          fill="currentColor"
          d="M12,21L15.6,16.2C14.6,15.45 13.35,15 12,15C10.65,15 9.4,15.45 8.4,16.2L12,21"
          opacity="0">
          <animate
            id="svgSpinnersWifi0"
            fill="freeze"
            attributeName="opacity"
            begin="0;svgSpinnersWifi1.end+0.2s"
            calcMode="discrete"
            dur="0.25s"
            values="0;1" />
          <animate
            id="svgSpinnersWifi1"
            fill="freeze"
            attributeName="opacity"
            begin="svgSpinnersWifi3.end+0.5s"
            dur="0.001s"
            values="1;0" />
        </path>
        <path
          fill="currentColor"
          d="M12,9C9.3,9 6.81,9.89 4.8,11.4L6.6,13.8C8.1,12.67 9.97,12 12,12C14.03,12 15.9,12.67 17.4,13.8L19.2,11.4C17.19,9.89 14.7,9 12,9Z"
          opacity="0">
          <animate
            id="svgSpinnersWifi2"
            fill="freeze"
            attributeName="opacity"
            begin="svgSpinnersWifi0.end"
            calcMode="discrete"
            dur="0.25s"
            values="0;1" />
          <animate
            fill="freeze"
            attributeName="opacity"
            begin="svgSpinnersWifi3.end+0.5s"
            dur="0.001s"
            values="1;0" />
        </path>
        <path
          fill="currentColor"
          d="M12,3C7.95,3 4.21,4.34 1.2,6.6L3,9C5.5,7.12 8.62,6 12,6C15.38,6 18.5,7.12 21,9L22.8,6.6C19.79,4.34 16.05,3 12,3"
          opacity="0">
          <animate
            id="svgSpinnersWifi3"
            fill="freeze"
            attributeName="opacity"
            begin="svgSpinnersWifi2.end"
            calcMode="discrete"
            dur="0.25s"
            values="0;1" />
          <animate
            fill="freeze"
            attributeName="opacity"
            begin="svgSpinnersWifi3.end+0.5s"
            dur="0.001s"
            values="1;0" />
        </path>
      </svg>
    </div>
  {/if}
</div>

<style>
  /* width */
  ::-webkit-scrollbar {
    width: 10px;
    margin: 2px;
  }

  /* Track */
  ::-webkit-scrollbar-track {
    border: solid 2px transparent;
    background: #00000000;
  }

  /* Handle */
  ::-webkit-scrollbar-thumb {
    margin: 1px;
    width: 2px;
    background: #fff;
  }

  /* Handle on hover */
  ::-webkit-scrollbar-thumb:hover {
    background: #ddd;
  }

  #link-one {
    animation: forwards flyInOne 3s;
  }

  #link-two {
    animation: forwards flyInTwo 3s;
  }

  #link-three {
    animation: forwards flyInThree 3s;
  }

  @keyframes flyInOne {
    0% {
      translate: 0 40px;
    }
    60% {
      translate: 0 40px;
    }
    80% {
      translate: 0 0;
    }
    100% {
      translate: 0 0;
    }
  }

  @keyframes flyInTwo {
    0% {
      translate: 0 40px;
    }
    65% {
      translate: 0 40px;
    }
    85% {
      translate: 0 0;
    }
    100% {
      translate: 0 0;
    }
  }

  @keyframes flyInThree {
    0% {
      translate: 0 40px;
    }
    70% {
      translate: 0 40px;
    }
    90% {
      translate: 0 0;
    }
    100% {
      translate: 0 0;
    }
  }
</style>
