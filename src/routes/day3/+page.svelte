<script>
	let isDropdownOpen = false;
	const triggerDropdown = () => {
		isDropdownOpen = !isDropdownOpen;
	};
	const handleDropdownFocusLoss = ({ relatedTarget, currentTarget }) => {
		if (relatedTarget instanceof HTMLElement && currentTarget.contains(relatedTarget)) return;
		isDropdownOpen = false;
	};
</script>

<svelte:head>
	<style>
		@import url("https://fonts.googleapis.com/css2?family=Montserrat+Alternates:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,100;1,200;1,300;1,400;1,500;1,600;1,700;1,800;1,900&family=Sometype+Mono:ital,wght@0,400..700;1,400..700&display=swap");
		body {
			font-family: "Montserrat Alternates", sans-serif;
			background-color: #4fabd4;
		}
	</style>
</svelte:head>

<nav class="p-4">
	<div>
		<button
			class="ml-auto block sm:hidden"
			on:click={triggerDropdown}
			on:focusout={handleDropdownFocusLoss}
		>
			<img src="/ducks/menu.svg" alt="Menu Icon" class="w-8" />
		</button>

		<div
			class="absolute right-4 top-16 flex scale-0 flex-col gap-2 rounded-md bg-[#577eb1] px-4 py-2 text-white transition-transform sm:hidden"
			class:scale-100={isDropdownOpen}
		>
			<span>Quack Facts</span>
			<span>Duckumentary</span>
			<span>QuackTube</span>
			<span class="font-semibold">Join the Flock</span>
		</div>
	</div>

	<div class="mt-4 hidden items-center justify-around gap-4 text-lg sm:flex lg:text-2xl">
		<span class="cursor-pointer underline-offset-2 hover:underline">Quack Facts</span>
		<span class="cursor-pointer underline-offset-2 hover:underline">Duckumentary</span>
		<span class="cursor-pointer underline-offset-2 hover:underline">QuackTube</span>
		<button class="rounded-2xl bg-[#577eb1] px-4 py-1 transition hover:bg-opacity-80">
			Join the Flock
		</button>
	</div>
</nav>

<main class="relative h-screen">
	<img
		class="absolute left-8 top-[20%] z-20 w-32 sm:w-56 md:w-72 lg:left-14 lg:top-1/4 lg:w-[360px]"
		src="/ducks/duck1.svg"
		alt="Duck 1"
	/>
	<img
		class="absolute left-1/2 top-1/3 z-20 w-24 sm:w-48 md:left-[40%] md:w-64 lg:w-80"
		src="/ducks/duck2.svg"
		alt="Duck 2"
	/>
</main>

<h1 class="absolute bottom-1/4 right-12 z-20 flex flex-col text-3xl font-medium sm:text-6xl">
	<span>Duck Dynasty</span>
	<span>Water Edition</span>
</h1>

<div class="relative -mt-1 h-[50vh] bg-[#577eb1]">
	<img
		src="/ducks/lilypad1.svg"
		alt="Lilypad 1"
		class="absolute -top-[35%] hidden w-48 rotate-12 -scale-x-100 sm:block lg:-left-24 lg:-top-[80%] lg:w-96"
	/>

	<img
		src="/ducks/lilypad1.svg"
		alt="Lilypad 1"
		class="absolute left-1/4 top-[25%] hidden w-24 -rotate-12 -scale-x-100 sm:block lg:-top-[60%] lg:left-1/4 lg:w-96"
	/>
	<img
		src="/ducks/lilypad2.svg"
		alt="Lilypad 2"
		class="absolute -top-[35%] right-0 hidden w-64 sm:block lg:-top-[100%] lg:w-96 xl:-top-[150%]"
	/>

	<div class="absolute bottom-1/2 right-1/4 h-16 w-16 rounded-full border-2 border-[#4fabd4]"></div>
	<div class="absolute bottom-1/3 right-1/3 h-12 w-12 rounded-full border-2 border-[#4fabd4]"></div>
	<div class="absolute bottom-[20%] right-1/4 h-8 w-8 rounded-full border-2 border-[#4fabd4]"></div>
</div>

<style>
	main {
		background-image: url("/ducks/water.svg");
		background-size: contain;
		background-position-y: bottom;
		background-repeat: no-repeat;
	}

	@media screen and (min-width: 1280px) {
		main {
			background-size: cover;
		}
	}
</style>
