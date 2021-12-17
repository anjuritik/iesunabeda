<style>
.under {
	background-image: linear-gradient(45deg, #fcdb6f, #fdcf01);
}

@media (min-width: 1024px) {
	.background {
		background-image: url('/home/bg-lighter.svg');
		/* background-image: url('/home/landscape-background.webp'); */
	}
}

@media (max-width: 1024px) {
	.background {
		/* background-image: url('/home/background.webp'); */
		background-image: url('/home/bg-lighter.svg');
	}
}
</style>

<script>
import GrnIndGradiantButton from '$lib/ui/GrnIndGradiantButton.svelte'
let loading = false
</script>

<section class="background bg-no-repeat bg-cover">
	<div class="container mx-auto max-w-7xl p-4 sm:p-10 lg:flex lg:items-start lg:justify-between">
		</div>

		<div class="pt-10 lg:pt-0 flex justify-center  lg:w-1/2">
			Institution of Engineers - Sunabeda Local Center
		</div>
	<div>
		<img src="{`/HomeSlide1.jpg`}" alt="IESunabeda" class=" object-cover mr-2  w-full h-96" />
	</div>
</section>
