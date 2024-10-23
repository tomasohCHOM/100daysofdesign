<script>
	const shoppingCart = [
		{
			title: 'CHARLI xcx brat 7" VINYL',
			price: 35.99
		},
		{
			title: "BEABADOOBEE THIS IS HOW TOMORROW MOVES ALTERNATIVE COVER VINYL",
			price: 42.99
		},
		{
			title: "THE 1975 LIVE FROM REAL WORLD STUDIOS 7” VINYL",
			price: 36.59
		}
	];

	const subtotal = shoppingCart.reduce((acc, item) => acc + item.price, 0);
	const taxes = subtotal * 0.24;
	const total = subtotal + taxes;
</script>

<svelte:head>
	<style>
		@import url("https://fonts.googleapis.com/css2?family=Sometype+Mono:ital,wght@0,400..700;1,400..700&display=swap");

		body {
			font-family: "Sometype Mono", monospace;
			background-color: #fff9f9;
		}
	</style>
</svelte:head>

<main class="grid gap-4 mx-auto max-w-screen-xl p-2">
	<img src="/ecommerce/grassbackground.png" alt="Grass Background Banner" class="w-full" />
	<div class="flex items-center justify-between text-xl">
		<span class="flex gap-1 cursor-pointer hover:underline underline-offset-4">
			<img src="/ecommerce/leftarrow.svg" alt="Left Arrow" class="w-5" />
			BACK TO CART
		</span>
		<span>VINLYZ.NET</span>
	</div>
	<section class="flex flex-col lg:flex-row gap-4 w-full">
		<div
			class="w-full p-2 lg:w-3/5 rounded-md flex items-center justify-center gap-4 md:gap-8 border border-black"
		>
			{#each [1, 2, 3] as i}
				<div class="relative">
					<img src="/ecommerce/cd{i}.png" alt={"CD " + i} />
					<div
						class="absolute bg-white right-0 top-4 text-xs w-6 h-6 sm:text-[1rem] sm:w-8 sm:h-8 flex items-center
            justify-center border border-black rounded-full"
					>
						x1
					</div>
				</div>
			{/each}
		</div>
		<div class="w-full lg:w-2/5 px-6 py-2 rounded-md border border-black">
			<h2 class="flex gap-1">
				<img src="/ecommerce/bag.svg" alt="Shopping Bag" class="w-3" /> SHOPPING CART
			</h2>
			<div class="border-b border-black border-dashed pb-4">
				<ol class="pl-3">
					{#each shoppingCart as item}
						<li class="text-sm flex gap-10 items-center justify-between">
							<span>{item.title}</span>
							<span>...${item.price}</span>
						</li>
					{/each}
				</ol>
			</div>
			<div class="mt-4 text-sm flex items-center justify-between">
				<span><span class="font-semibold">SUBTOTAL:</span> ${subtotal.toFixed(2)}</span>
				<span><span class="font-semibold">TAXES:</span> ${taxes.toFixed(2)}</span>
			</div>
			<div class="mt-2 text-sm flex items-center justify-between">
				<span><span class="font-semibold">SHIPPING:</span>SHIPPING: PICKUP, FREE</span>
				<span><b>TOTAL: ${total.toFixed(2)}</b></span>
			</div>
		</div>
	</section>
	<section class="grid grid-cols-1 lg:grid-cols-2 gap-4">
		<div class="rounded-md border flex flex-col sm:flex-row gap-4 border-black p-4">
			<div class="text-sm w-full sm:w-1/2 flex flex-col gap-8">
				<h3 class="flex gap-1">
					<img src="/ecommerce/card.svg" alt="Credit Card" class="w-4" />
					PAYMENT METHOD
				</h3>
				<div class="flex flex-col">
					<span>CONTACT</span>
					<span>christinex143@gmail.com</span>
				</div>
				<div class="flex flex-col">
					<span>SHIPPING TO</span>
					<span>South Costa Plaza</span>
				</div>
				<div class="flex flex-col">
					<span>SHIPPING METHOD</span>
					<span>Pick up only</span>
				</div>
				<button class="border border-black p-2 rounded-md bg-[#ff7539] sm:w-[80%]">
					MAKE SOME CHANGES
				</button>
			</div>
			<div class="flex flex-col gap-4 text-sm">
				<div>
					<label for="card-number">CARD NUMBER</label>
					<input id="card-number" class="p-2 w-full border border-black rounded-lg" />
				</div>
				<div>
					<label for="card-name">NAME ON CARD</label>
					<input id="card-name" class="p-2 w-full border border-black rounded-lg" />
				</div>
				<div>
					<label for="expiration">EXPIRATION DATE</label>
					<input id="expiration" class="p-2 w-full border border-black rounded-lg" />
				</div>
				<div>
					<label for="cvv">CVV</label>
					<input id="cvv" class="p-2 w-full border border-black rounded-lg" />
				</div>
				<div>
					<input id="save-card" type="checkbox" class="scale-125" />
					<label class="text-xs" for="save-card">SAVE CREDIT CARD INFOR FOR NEXT TIME</label>
				</div>
				<button class="border border-black p-2 rounded-md bg-[#8894ff] w-full">
					CONFIRM MY PURCHASE
				</button>
			</div>
		</div>
		<div>
			<img src="/ecommerce/promo.png" alt="Promo Banner" class="w-full" />
		</div>
	</section>
</main>
