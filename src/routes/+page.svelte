<script>
	const submissions = [
		{ day: 2, title: "Vinlyz.net E-Commerce Site", username: "t_1907" },
		{ day: 3, title: "Duck Dynasty Water Edition", username: "demonicgoat" },
		{ day: 4, title: "Baymax Calculator", username: "bergerboyyy" },
		{ day: 14, title: "Debut Album Release", username: "semsema" },
		{ day: 25, title: "ACM Design", username: "bergerboyyy" }
	];
</script>

<div class="mt-8 flex flex-col items-center">
	<div class="ball relative h-[350px] md:h-[600px]">
		<img
			src="/acm.svg"
			alt="ACM Icon"
			class="absolute left-1/2 top-[40%] max-w-[8rem] -translate-x-1/2 -translate-y-1/2 md:max-w-[16rem]"
		/>
		<img src="flower.svg" alt="Flower" class="absolute -left-28 bottom-6 z-20 w-40" />
		<img src="flower-faded.svg" alt="Flower" class="absolute -right-28 bottom-6 z-20 w-40" />

		<img src="/capy1.svg" alt="Capybara 1" class="absolute bottom-6 left-28 z-20 w-40" />
		<img src="/capy2.svg" alt="Capybara 1" class="absolute bottom-6 right-28 z-20 w-40" />
		<div
			class="absolute -bottom-16 left-1/2 h-32 w-[20rem] -translate-x-1/2 rounded-full bg-[#fc7373] md:w-[30rem]"
		/>
	</div>
	<main class="flex h-[80vh] w-full flex-col gap-4 bg-[#fc7373] py-24 text-white sm:flex-row">
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

<!-- <img src="/flower.svg" alt="ACM Icon" class="max-w-[24rem]" />
<img src="/flower-faded.svg" alt="ACM Icon" class="max-w-[24rem]" /> -->

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
