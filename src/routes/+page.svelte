<script>
	const submissions = [
		{ day: 2, title: "Vinlyz.net E-Commerce Site", username: "t_1907" },
		{ day: 3, title: "Duck Dynasty Water Edition", username: "demonicgoat" },
		{ day: 4, title: "Baymax Calculator", username: "bergerboyyy" },
		{ day: 14, title: "Debut Album Release", username: "semsema" },
		{ day: 25, title: "ACM Design", username: "bergerboyyy" }
	];
</script>

<div class="relative mt-8 flex flex-col items-center overflow-hidden">
	<div class="ball relative h-[350px] md:h-[600px]">
		<img
			src="/acm.svg"
			alt="ACM Icon"
			class="absolute left-1/2 top-[40%] max-w-[8rem] -translate-x-1/2 -translate-y-1/2 md:max-w-[16rem]"
		/>

		<!-- Flowers (Left side) -->
		<img
			src="flower1.svg"
			alt="Flower"
			class="absolute -left-56 bottom-8 w-[13rem] -rotate-45 opacity-60 md:-left-[280px] md:w-[23rem]"
		/>
		<img
			src="flower2.svg"
			alt="Flower"
			class="absolute -bottom-24 -left-56 w-40 -rotate-[30deg] -scale-x-100 opacity-80 md:-left-72 md:w-64"
		/>
		<img
			src="flower1.svg"
			alt="Flower"
			class="absolute -bottom-8 -left-44 w-[15rem] md:-left-64 md:w-[23rem]"
		/>
		<img
			src="flower2.svg"
			alt="Flower"
			class="absolute -bottom-32 -left-40 w-40 rotate-[30deg] opacity-60 md:-bottom-48 md:-left-52 md:w-64"
		/>
		<!-- Flowers (Right side) -->
		<img
			src="flower3.svg"
			alt="Flower"
			class="absolute -bottom-8 -right-20 w-24 md:-bottom-24 md:-right-28 md:w-40"
		/>
		<img
			src="flower3.svg"
			alt="Flower"
			class="absolute -right-40 bottom-12 w-32 -rotate-[30deg] -scale-x-100 md:bottom-24 md:w-40"
		/>
		<img
			src="flower3.svg"
			alt="Flower"
			class="absolute -bottom-16 -right-44 w-20 -rotate-12 opacity-60 md:-bottom-24 md:-right-64 md:w-32"
		/>
		<img
			src="flower1.svg"
			alt="Flower"
			class="absolute -bottom-12 -right-48 w-48 -rotate-[30deg] opacity-50 md:-right-72 md:w-80"
		/>

		<img
			src="/capy1.svg"
			alt="Capybara 1"
			class="absolute bottom-6 left-16 z-20 w-24 md:left-28 md:w-40"
		/>
		<img
			src="/capy2.svg"
			alt="Capybara 1"
			class="absolute bottom-6 right-16 z-20 w-24 md:right-28 md:w-40"
		/>
		<div
			class="absolute -bottom-16 left-1/2 h-32 w-[20rem] -translate-x-1/2 rounded-full bg-[#fc7373] md:w-[30rem]"
		/>
	</div>
	<main class="relative flex w-full flex-col gap-4 bg-[#fc7373] py-24 text-white sm:flex-row">
		<p class="absolute right-4 top-4 text-right text-[0.75rem] font-semibold text-white">
			Designed by @bergerboyyy (Day 25 Submission)
		</p>
		<section class="flex max-w-[768px] flex-col gap-2 p-8">
			<h1 class="text-4xl font-bold">100 Days Of Design Challenge</h1>
			<p>
				A compilation of some of ACM CSUF's <span>Design Team</span> favorite designs from the
				<b>100 Days of Design</b> Challenge.
			</p>
			<div class="max-w-max pl-4">
				{#each submissions as submission}
					<a class="group flex gap-1" href="/day{submission.day}">
						<span class="underline-offset-2 group-hover:underline">
							{submission.title} (by @{submission.username}) - Day {submission.day} Submission
						</span>
						<img
							src="/diagonalarrow.svg"
							alt="Link Icon"
							class="transition-transform group-hover:-translate-y-1 group-hover:translate-x-1"
						/>
					</a>
				{/each}
			</div>
		</section>
		<img src="/acmdesign.svg" alt="ACM Design Icon" class="max-w-[24rem]" />
	</main>
</div>

<style>
	@import url("https://fonts.googleapis.com/css2?family=Poppins:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,100;1,200;1,300;1,400;1,500;1,600;1,700;1,800;1,900&display=swap");

	main {
		font-family: "Poppins", sans-serif;
	}

	.ball {
		/* height: 600px; */
		aspect-ratio: 1;
		border-radius: 50%;
		background: radial-gradient(50% 50% at 50% 50%, #ffd7d7 0%, #ffacac 100%);
	}
</style>
