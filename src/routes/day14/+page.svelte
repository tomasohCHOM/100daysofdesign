<svelte:head>
	<style>
		@import url("https://fonts.googleapis.com/css2?family=Aldrich&display=swap");

		:root {
			color-scheme: dark;
		}

		body {
			font-family: "Aldrich", sans-serif;
			background-color: #222222;
			color: white;
		}
	</style>
</svelte:head>

<div class="flex h-screen w-full items-center justify-center">
	<main class="relative h-[668.8px] w-[min(1024px,90vw)]">
		<div class="flex h-full flex-col">
			<h1 class="mt-48 text-center text-3xl md:text-5xl">DEBUT ALBUM RELEASE</h1>
			<div class="mt-4 flex items-center justify-center gap-6">
				<div
					class="flex w-20 flex-col items-center rounded-xl bg-[#d7ffb0] bg-opacity-25 p-4 md:w-32"
				>
					<span class="text-2xl md:text-6xl">63</span>
					<span class="md:text-2xl">days</span>
				</div>
				<div
					class="flex w-20 flex-col items-center rounded-xl bg-[#d7ffb0] bg-opacity-25 p-4 md:w-32"
				>
					<span class="text-2xl md:text-6xl">9</span>
					<span class="md:text-2xl">hours</span>
				</div>
				<div
					class="flex w-20 flex-col items-center rounded-xl bg-[#d7ffb0] bg-opacity-25 p-4 md:w-32"
				>
					<span class="text-2xl md:text-6xl">10</span>
					<span class="md:text-2xl">mins</span>
				</div>
			</div>

			<a
				href="https://open.spotify.com/prerelease/5nlyRaHZKCezRCf1Buhtkm?si=84e1952d1f7f4161&nd=1&dlsi=32786b390d9942e5"
				class="mx-auto mt-8 block max-w-max text-center text-2xl underline"
				target="_blank"
			>
				Pre-Save Escaper here
			</a>

			<footer class="mb-4 mt-auto flex items-center justify-between px-4">
				<div class="flex items-center gap-1 text-[0.75rem] sm:text-[1rem]">
					<img src="/debut/spotify.svg" alt="Spotify Icon" class="w-6" /> Sarah Kinsley
				</div>
				<p class="text-right text-[0.625rem] sm:text-[1rem]">
					STREAM 'Last Time We Never Meet again' NOW
				</p>
			</footer>
		</div>
	</main>
</div>

<style>
	main {
		background: url("/debut/album-image.png") rgba(176, 160, 144, 0.4) 100% / cover no-repeat;
		background-size: contain;
		background-repeat: no-repeat;
		background-blend-mode: overlay;
		/* padding-top: 65.31%; */
	}
</style>
