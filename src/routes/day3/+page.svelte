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
			class="sm:hidden block ml-auto"
			on:click={triggerDropdown}
			on:focusout={handleDropdownFocusLoss}
		>
			<img src="/ducks/menu.svg" alt="Menu Icon" class="w-8" />
		</button>

		<div
			class="sm:hidden transition-transform absolute scale-0 bg-[#577eb1] rounded-md py-2 px-4 flex flex-col gap-2 right-4 top-16 text-white"
			class:scale-100={isDropdownOpen}
		>
			<span>Quack Facts</span>
			<span>Duckumentary</span>
			<span>QuackTube</span>
			<span class="font-semibold">Join the Flock</span>
		</div>
	</div>

	<div class="hidden sm:flex items-center justify-around gap-4 text-lg lg:text-2xl mt-4">
		<span class="hover:underline underline-offset-2 cursor-pointer">Quack Facts</span>
		<span class="hover:underline underline-offset-2 cursor-pointer">Duckumentary</span>
		<span class="hover:underline underline-offset-2 cursor-pointer">QuackTube</span>
		<button class="bg-[#577eb1] px-4 py-1 rounded-2xl hover:bg-opacity-80 transition">
			Join the Flock
		</button>
	</div>
</nav>

<main class="h-screen relative">
	<img
		class="z-20 absolute w-32 sm:w-56 md:w-72 lg:w-[360px] lg:left-14 top-[20%] left-8 lg:top-1/4"
		src="/ducks/duck1.svg"
		alt="Duck 1"
	/>
	<img
		class="z-20 absolute w-24 sm:w-48 md:w-64 lg:w-80 left-1/2 md:left-[40%] top-1/3"
		src="/ducks/duck2.svg"
		alt="Duck 2"
	/>
</main>

<h1 class="flex z-20 flex-col font-medium text-3xl sm:text-6xl right-12 bottom-1/4 absolute">
	<span>Duck Dynasty</span>
	<span>Water Edition</span>
</h1>

<div class="h-[50vh] bg-[#577eb1] -mt-1 relative">
	<img
		src="/ducks/lilypad1.svg"
		alt="Lilypad 1"
		class="hidden sm:block absolute -scale-x-100 w-48 lg:w-96 -top-[35%] lg:-top-[80%] lg:-left-24 rotate-12"
	/>

	<img
		src="/ducks/lilypad1.svg"
		alt="Lilypad 1"
		class="hidden sm:block absolute -scale-x-100 w-24 lg:w-96 left-1/4 top-[25%] lg:-top-[60%] lg:left-1/4 -rotate-12"
	/>
	<img
		src="/ducks/lilypad2.svg"
		alt="Lilypad 2"
		class="hidden sm:block absolute w-64 lg:w-96 right-0 -top-[35%] lg:-top-[100%] xl:-top-[150%]"
	/>

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

	@media screen and (min-width: 1280px) {
		main {
			background-size: cover;
		}
	}
</style>
