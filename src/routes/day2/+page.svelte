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

<main class="mx-auto grid max-w-screen-xl gap-4 p-2">
	<img src="/ecommerce/grassbackground.png" alt="Grass Background Banner" class="w-full" />
	<div class="flex items-center justify-between text-xl">
		<span class="flex cursor-pointer gap-1 underline-offset-4 hover:underline">
			<img src="/ecommerce/leftarrow.svg" alt="Left Arrow" class="w-5" />
			BACK TO CART
		</span>
		<span>VINLYZ.NET</span>
	</div>
	<section class="flex w-full flex-col gap-4 lg:flex-row">
		<div
			class="flex w-full items-center justify-center gap-4 rounded-md border border-black p-2 md:gap-8 lg:w-3/5"
		>
			{#each [1, 2, 3] as i}
				<div class="relative">
					<img src="/ecommerce/cd{i}.png" alt={"CD " + i} />
					<div
						class="absolute right-0 top-4 flex h-6 w-6 items-center justify-center rounded-full border border-black bg-white
            text-xs sm:h-8 sm:w-8 sm:text-[1rem]"
					>
						x1
					</div>
				</div>
			{/each}
		</div>
		<div class="w-full rounded-md border border-black px-6 py-2 lg:w-2/5">
			<h2 class="flex gap-1">
				<img src="/ecommerce/bag.svg" alt="Shopping Bag" class="w-3" /> SHOPPING CART
			</h2>
			<div class="border-b border-dashed border-black pb-4">
				<ol class="pl-3">
					{#each shoppingCart as item}
						<li class="flex items-center justify-between gap-10 text-sm">
							<span>{item.title}</span>
							<span>...${item.price}</span>
						</li>
					{/each}
				</ol>
			</div>
			<div class="mt-4 flex items-center justify-between text-sm">
				<span><span class="font-semibold">SUBTOTAL:</span> ${subtotal.toFixed(2)}</span>
				<span><span class="font-semibold">TAXES:</span> ${taxes.toFixed(2)}</span>
			</div>
			<div class="mt-2 flex items-center justify-between text-sm">
				<span><span class="font-semibold">SHIPPING:</span>SHIPPING: PICKUP, FREE</span>
				<span><b>TOTAL: ${total.toFixed(2)}</b></span>
			</div>
		</div>
	</section>
	<section class="grid grid-cols-1 gap-4 lg:grid-cols-2">
		<div class="flex flex-col gap-4 rounded-md border border-black p-4 sm:flex-row">
			<div class="flex w-full flex-col gap-8 text-sm sm:w-1/2">
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
				<button class="rounded-md border border-black bg-[#ff7539] p-2 sm:w-[80%]">
					MAKE SOME CHANGES
				</button>
			</div>
			<div class="flex flex-col gap-4 text-sm">
				<div>
					<label for="card-number">CARD NUMBER</label>
					<input id="card-number" class="w-full rounded-lg border border-black p-2" />
				</div>
				<div>
					<label for="card-name">NAME ON CARD</label>
					<input id="card-name" class="w-full rounded-lg border border-black p-2" />
				</div>
				<div>
					<label for="expiration">EXPIRATION DATE</label>
					<input id="expiration" class="w-full rounded-lg border border-black p-2" />
				</div>
				<div>
					<label for="cvv">CVV</label>
					<input id="cvv" class="w-full rounded-lg border border-black p-2" />
				</div>
				<div>
					<input id="save-card" type="checkbox" class="scale-125" />
					<label class="text-xs" for="save-card">SAVE CREDIT CARD INFOR FOR NEXT TIME</label>
				</div>
				<button class="w-full rounded-md border border-black bg-[#8894ff] p-2">
					CONFIRM MY PURCHASE
				</button>
			</div>
		</div>
		<div>
			<img src="/ecommerce/promo.png" alt="Promo Banner" class="w-full" />
		</div>
	</section>
</main>
