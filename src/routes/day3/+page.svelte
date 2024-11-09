<svelte:head>
	<style>
		@import url("https://fonts.googleapis.com/css2?family=Montserrat+Alternates:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,100;1,200;1,300;1,400;1,500;1,600;1,700;1,800;1,900&family=Sometype+Mono:ital,wght@0,400..700;1,400..700&display=swap");
		body {
			font-family: "Montserrat Alternates", sans-serif;
			background-color: #4fabd4;
		}
	</style>
</svelte:head>

<main class="h-screen">
	<nav>
		<div class="hidden sm:flex items-center justify-around gap-4 text-lg lg:text-2xl mt-4">
			<span class="hover:underline underline-offset-2 cursor-pointer">Quack Facts</span>
			<span class="hover:underline underline-offset-2 cursor-pointer">Duckumentary</span>
			<span class="hover:underline underline-offset-2 cursor-pointer">QuackTube</span>
			<button class="bg-[#577eb1] px-4 py-1 rounded-2xl hover:bg-opacity-80 transition">
				Join the Flock
			</button>
		</div>
	</nav>

	<img class="absolute w-32 lg:w-96 left-14 top-1/4" src="/ducks/duck1.svg" alt="Duck 1" />
	<img class="absolute w-24 lg:w-80 left-1/3 top-1/3" src="/ducks/duck2.svg" alt="Duck 2" />
</main>

<h1 class="flex z-20 flex-col font-medium text-3xl sm:text-6xl right-12 bottom-1/4 absolute">
	<span>Duck Dynasty</span>
	<span>Water Edition</span>
</h1>

<div class="h-[50vh] bg-[#577eb1] -mt-1 relative">
	<div class="absolute border-[#4fabd4] border-2 bottom-1/2 right-1/4 rounded-full w-16 h-16"></div>
	<div class="absolute border-[#4fabd4] border-2 bottom-1/3 right-1/3 rounded-full w-12 h-12"></div>
	<div class="absolute border-[#4fabd4] border-2 bottom-[20%] right-1/4 rounded-full w-8 h-8"></div>
</div>

<style>
	main {
		background-image: url("/ducks/water.svg");
		background-size: contain;
		background-position-y: bottom;
		background-repeat: no-repeat;
	}

	@media screen and (min-width: 1024px) {
		main {
			background-size: cover;
		}
	}
</style>
