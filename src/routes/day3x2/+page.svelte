<svelte:head>
	<style>
		@import url("https://fonts.googleapis.com/css2?family=Kumbh+Sans:wght@100..900&display=swap");
		:root {
			color: #fff;
			font-family: "Kumbh Sans";
			font-size: 20px;
			font-style: normal;
			font-weight: 400;
			line-height: normal;
			letter-spacing: 4px;
			text-transform: uppercase;

			color-scheme: dark;
		}
		body {
			background-color: #222222;
		}
	</style>
</svelte:head>

<main class="relative">
	<nav class="flex items-center gap-8 px-6 py-4">
		<img src="/cyberpunk/logo.svg" alt="Cyberpunk Logo" />
		<div class="flex gap-6">
			<span>HOME</span>
			<span>ABOUT</span>
			<span>COMMUNITIES</span>
			<span>NEWS</span>
		</div>
	</nav>

	<div class="absolute right-[20%] top-1/3">
		<img src="/cyberpunk/cyber.svg" alt="Cyber" class="w-80" />
	</div>
	<div class="absolute right-[10%] top-[42%]">
		<img src="/cyberpunk/punk.svg" alt="Punk" class="w-96" />
	</div>

	<img src="/cyberpunk/socials.svg" alt="Social Media Links" class="absolute left-10 top-1/3" />

	<div class="absolute left-10 top-3/4">
		<p class="text-sm font-semibold text-[#01e4ad]">"THERE IS A MONSTER"</p>
		<p class="text-xs">INSIDE ALL OF <b>US</b></p>
		<button class="play-btn mt-4 border-2 border-white px-6 py-3 text-sm">PLAY NOW</button>
	</div>

	<div class="character-model absolute right-[4%] top-6 w-96"></div>
	<div class="absolute right-[4%] top-6 flex w-96 flex-col items-center">
		<img src="/cyberpunk/character.svg" alt="Character Model" />
		<p class="text-[0.5rem]">MADE BY KRISTEN &lt;3</p>
	</div>
</main>

<style>
	main {
		height: 100vh;
		background: linear-gradient(
			180deg,
			rgba(49, 1, 88, 0.2) 53.5%,
			rgba(104, 52, 132, 0.3) 80%,
			rgba(150, 95, 169, 0.25) 100%
		);
		background-image: url("/cyberpunk/cyberpunk.svg");
		background-size: cover;
		background-position-y: bottom;
		background-repeat: no-repeat;
	}
	.play-btn {
		filter: drop-shadow(0px 0px 10px #fff);
	}

	.character-model {
		/* opacity: 0.4; */
		background: linear-gradient(
			180deg,
			rgba(36, 0, 255, 0) 7%,
			rgba(206, 8, 8, 0.17) 45.5%,
			rgba(255, 255, 255, 0.4) 100%
		);
		backdrop-filter: blur(10px);
	}
</style>
