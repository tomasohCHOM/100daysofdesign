<script>
	const submissions = [
		{ day: 2, title: "Vinlyz.net E-Commerce Site", username: "t_1907" },
		{ day: 3, title: "Duck Dynasty Water Edition", username: "demonicgoat" },
		{ day: 4, title: "Baymax Calculator", username: "bergerboyyy" },
		{ day: 14, title: "Debut Album Release", username: "semsema" }
	];
</script>

<main class="flex flex-col gap-4 sm:flex-row">
	<section class="flex max-w-[768px] flex-col gap-2 p-8">
		<h1 class="text-4xl font-semibold">100 Days Of Design Challenge</h1>
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

<style>
	@import url("https://fonts.googleapis.com/css2?family=Poppins:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,100;1,200;1,300;1,400;1,500;1,600;1,700;1,800;1,900&display=swap");

	main {
		font-family: "Poppins", sans-serif;
	}
</style>
