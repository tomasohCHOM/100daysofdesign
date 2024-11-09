<svelte:head>
	<style>
		@import url("https://fonts.googleapis.com/css2?family=Aldrich&family=Montserrat+Alternates:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,100;1,200;1,300;1,400;1,500;1,600;1,700;1,800;1,900&family=Sometype+Mono:ital,wght@0,400..700;1,400..700&display=swap");
		body {
			font-family: "Aldrich", sans-serif;
			background-color: #222222;
			color: white;
		}
	</style>
</svelte:head>

<div class="flex h-screen w-full items-center justify-center">
	<main class="relative h-full w-[min(1024px,90vw)]">
		<div class="absolute left-0 right-0 top-1/3">
			<h1 class="text-center text-5xl">DEBUT ALBUM RELEASE</h1>
			<div class="flex items-center justify-center">
				<div class="rounded-xl p-4">
					<span>63</span>
					<span>days</span>
				</div>
				<div>
					<span>9</span>
					<span>hours</span>
				</div>
				<div>
					<span>10</span>
					<span>minutes</span>
				</div>
			</div>
		</div>
	</main>
</div>

<style>
	main {
		background: url("/debut/album-image.png") rgba(205, 190, 175, 0.4) 100% / cover no-repeat;
		background-size: contain;
		background-repeat: no-repeat;
		background-blend-mode: overlay;
		padding-top: 65.31%;
	}
</style>
