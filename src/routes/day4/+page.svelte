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

<h1 class="font-bold text-3xl p-2 mx-auto max-w-max text-slate-800">Baymax Calculator</h1>

<main class="py-4 max-w-screen-md mx-auto relative h-screen">
	<img src="/baymax/leg.svg" alt="Baymax Leg" class="absolute left-[28%] top-[77%] -scale-x-100" />
	<img src="/baymax/leg.svg" alt="Baymax Leg" class="absolute right-[28%] top-[77%]" />

	<img src="/baymax/body.svg" alt="Baymax Body" class="absolute top-[28%] left-0 right-0 mx-auto" />

	<img src="/baymax/arm.svg" alt="Baymax Arm" class="absolute top-[35%] left-[12%] -scale-x-100" />
	<img src="/baymax/arm.svg" alt="Baymax Arm" class="absolute top-[35%] right-[12%]" />

	<img src="/baymax/head.svg" alt="Baymax Head" class="absolute left-0 right-0 mx-auto" />

	<div class="absolute top-[18%] left-[35%] w-6 h-6 bg-black rounded-full"></div>
	<div class="absolute top-[18%] left-[61%] w-6 h-6 bg-black rounded-full"></div>
	<img
		src="/baymax/mouth.svg"
		alt="Baymax Mouth"
		class="absolute left-0 right-0 mx-auto top-[20%]"
	/>

	<div class="absolute top-[38%] left-0 right-0 mx-auto max-w-max">
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
			<button class="{buttonClassDefault} min-w-full col-span-2">0</button>
			<button class={buttonClassDefault}>.</button>
			<button class="{buttonClassDefault} bg-white row-span-2">=</button>
		</div>
		<div class="flex flex-col bg-gray-800 rounded-lg text-white p-2">
			<span class="text-right text-xs text-gray-400">2 + 5</span>
			<span class="text-right">7</span>
		</div>
	</div>
</main>
