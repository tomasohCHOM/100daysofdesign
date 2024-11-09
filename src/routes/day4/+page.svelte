<script>
	const buttonClass =
		"rounded-full w-11 h-11 flex items-center justify-center text-lg font-medium focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-gray-500 transition-colors";

	const buttonClassDefault = buttonClass + " bg-[#d2d2d2] hover:bg-[#cecece]";
	const buttonClassPink = buttonClass + " bg-[#ffd0d0] hover:bg-[#ffd9d9]";
	const buttonClassWhite = buttonClass + " bg-white hover:bg-gray-100";
</script>

<svelte:head>
	<style>
		body {
			background-color: #ececec;
		}
	</style>
</svelte:head>

<h1 class="mx-auto max-w-max p-8 px-2 text-3xl font-bold text-slate-800">Baymax Calculator</h1>

<p class="mx-auto max-w-sm p-4 text-center text-lg md:hidden">
	Baymax calculator does not look good in screen sizes smaller than 768px. Please use a larger
	screen size to view the Baymax calculator! :D
</p>

<main class="relative mx-auto hidden h-[695px] max-w-screen-md py-4 md:block">
	<img src="/baymax/leg.svg" alt="Baymax Leg" class="absolute left-[28%] top-[77%] -scale-x-100" />
	<img src="/baymax/leg.svg" alt="Baymax Leg" class="absolute right-[28%] top-[77%]" />

	<img src="/baymax/body.svg" alt="Baymax Body" class="absolute left-0 right-0 top-[28%] mx-auto" />

	<img src="/baymax/arm.svg" alt="Baymax Arm" class="absolute left-[12%] top-[35%] -scale-x-100" />
	<img src="/baymax/arm.svg" alt="Baymax Arm" class="absolute right-[12%] top-[35%]" />

	<img src="/baymax/head.svg" alt="Baymax Head" class="absolute left-0 right-0 mx-auto" />

	<div class="absolute left-[35%] top-[18%] h-6 w-6 rounded-full bg-black"></div>
	<div class="absolute left-[61%] top-[18%] h-6 w-6 rounded-full bg-black"></div>
	<img
		src="/baymax/mouth.svg"
		alt="Baymax Mouth"
		class="absolute left-0 right-0 top-[20%] mx-auto"
	/>

	<div class="absolute left-0 right-0 top-[38%] mx-auto max-w-max">
		<div class="grid grid-cols-4 gap-2">
			<button class={buttonClassPink}>CE</button>
			<button class={buttonClassPink}>C</button>
			<button class={buttonClassWhite}>+/-</button>
			<button class={buttonClassWhite}>/</button>
			<button class={buttonClassDefault}>7</button>
			<button class={buttonClassDefault}>8</button>
			<button class={buttonClassDefault}>9</button>
			<button class={buttonClassWhite}>x</button>
			<button class={buttonClassDefault}>4</button>
			<button class={buttonClassDefault}>5</button>
			<button class={buttonClassDefault}>6</button>
			<button class={buttonClassWhite}>-</button>
			<button class={buttonClassDefault}>1</button>
			<button class={buttonClassDefault}>2</button>
			<button class={buttonClassDefault}>3</button>
			<button class={buttonClassWhite}>+</button>
			<button class="{buttonClassDefault} col-span-2 min-w-full">0</button>
			<button class={buttonClassDefault}>.</button>
			<button class="{buttonClassDefault} row-span-2 bg-white">=</button>
		</div>
		<div class="flex flex-col rounded-lg bg-gray-800 p-2 text-white">
			<span class="text-right text-xs text-gray-400">2 + 5</span>
			<span class="text-right">7</span>
		</div>
	</div>
</main>
