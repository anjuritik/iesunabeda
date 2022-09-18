<style>
.nav {
	margin-left: 0.5rem;
	margin-right: 0.5rem;
	padding: 0.25rem 0.75rem;
	border-radius: 0.5rem;
	text-transform: uppercase;
	display: block;
}
.btn {
	display: block;
	background-image: url(/right-shadow.svg), url(/right-chevron.svg);
	background-position: 107% 100%, 90% 50%;
	background-size: auto 140%, 6px 740px;
	background-repeat: no-repeat, no-repeat;
	background-attachment: scroll, scroll;
}
.btn-yellow {
	box-shadow: 1px 1px 3px 0 #fdc700;
	background-color: #fdc700;
	padding-left: 2rem;
	padding-right: 2rem;
	font-weight: 600;
	--text-opacity: 1;
	color: #000;
	color: rgba(0, 0, 0, var(--text-opacity));
	transition-property: background-color, border-color, color, fill, stroke, opacity, box-shadow,
		transform;
	transition-duration: 0.5s;
	transition-timing-function: cubic-bezier(0.4, 0, 0.2, 1);
	--transform-translate-x: 0;
	--transform-translate-y: 0;
	--transform-rotate: 0;
	--transform-skew-x: 0;
	--transform-skew-y: 0;
	--transform-scale-x: 1;
	--transform-scale-y: 1;
	transform: translateX(var(--transform-translate-x)) translateY(var(--transform-translate-y))
		rotate(var(--transform-rotate)) skewX(var(--transform-skew-x)) skewY(var(--transform-skew-y))
		scaleX(var(--transform-scale-x)) scaleY(var(--transform-scale-y));
}
.frosted {
	backdrop-filter: blur(12px);
	background-color: hsla(0, 0%, 100%, 0.6);
}
</style>

<script>
import GrnIndGradiantButton from '$lib/ui/GrnIndGradiantButton.svelte'
import { Menu } from 'svelte-hero-icons'

let loading = false
let showSidebar = false

function getLoginUrl() {
	return `https://admin.misiki.in/otplogin`
}
function toggle() {
	return (showSidebar = !showSidebar)
}
function closeSidebar() {
	return (showSidebar = false)
}
</script>

<nav class="w-full fixed top-0 z-50 frosted shadow">
	<div class="container mx-auto max-w-7xl px-2 sm:px-10">
		<div class="flex items-center justify-between py-3">
			<div class="flex flex-wrap items-center justify-center lg:justify-start text-center w-full">
				<a
					href="/"
					title="Home"
					rel="prefetch"
					aria-label="IEI Sunabeda"
					class="
              flex
              items-center
              text-3xl
              font-bold
              underline
            ">
					<img src="{`/icon.png`}" alt="IESunabeda" class="h-24 mr-2" />
				</a>
				<div class=" text-sm lg:text-xl   lg:block font-sans font-bold" style="color-blue"> 
   Institution of Engineers- Sunabeda Local Center </div>
			</div>
			<div
				class="
            items-center
            flex-shrink-0
            text-xs
            font-semibold
            tracking-wide
			 lg:flex 
          ">
		  <div class=" items-center   bg-blue-100  px-6 py-2 rounded border  border-blue-300">
				<a href="/">Home</a>
				</div>
			
				<div class=" items-center bg-green-100  px-6 py-2 rounded border  border-green-300">
				<a href="/contacts">Contact Us</a>
				</div>
				<div class=" items-center bg-yellow-100  px-6 py-2 rounded border   border-yellow-300">
				<a href="/academics">Awards</a>
				</div>
<div class=" items-center bg-red-100  px-6 py-2 rounded border  border-red-300">
				<a href="/members">Members</a>
				</div>
				


<div class=" items-center  bg-purple-100 px-6 py-2 rounded border  border-purple-300">
				<a href="/halloffame">Forms</a>
				</div>
			</div>

				<aside class="z-50 sm:hidden">
					<div
						on:click="{toggle}"
						class="bg-gray-200 rounded-md flex items-center justify-center h-8 w-8">
						{#if !showSidebar}
							<svg
								xmlns="http://www.w3.org/2000/svg"
								class="h-6 w-6"
								fill="none"
								viewBox="0 0 24 24"
								stroke="currentColor">
								<path
									stroke-linecap="round"
									stroke-linejoin="round"
									stroke-width="2"
									d="M4 6h16M4 12h16M4 18h16"></path>
							</svg>
						{:else}
							<svg
								xmlns="http://www.w3.org/2000/svg"
								class="h-6 w-6"
								fill="none"
								viewBox="0 0 24 24"
								stroke="currentColor">
								<path
									stroke-linecap="round"
									stroke-linejoin="round"
									stroke-width="2"
									d="M6 18L18 6M6 6l12 12"></path>
							</svg>
						{/if}
					</div>
				</aside>

				<!-- <button
            aria-label="Open Menu"
            class="p-2 bg-gray-100 rounded focus:outline-none lg:hidden"
          >
            <svg
              fill="none"
              xmlns="http://www.w3.org/2000/svg"
              class="w-6 h-6 fill-current"
            >
              <path
                fill-rule="evenodd"
                clip-rule="evenodd"
                d="M2 12a1 1 0 011-1h18a1 1 0 110 2H3a1 1 0 01-1-1zM2 6a1 1 0
              011-1h18a1 1 0 110 2H3a1 1 0 01-1-1zM2 18a1 1 0 011-1h18a1 1 0
              110 2H3a1 1 0 01-1-1z"
              ></path>
            </svg>
          </button> -->
		</div>
	</div>

	{#if showSidebar}
		<div class="absolute z-40 inset-0 h-screen bg-white animate-slide">
			<div class="px-6 py-14 flex flex-col space-y-5">
				<a
					href="/about"
					title="About"
					class="mr-5 flex items-center space-x-2 text-gray-800 active:text-primary-700"
					on:click="{closeSidebar}">
					<h6 class="flex-1">About</h6>
				</a>

			</div>
		</div>
	{/if}
</nav>
