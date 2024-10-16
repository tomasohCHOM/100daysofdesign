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

<main class="grid gap-4 mx-auto max-w-screen-xl py-2">
	<img src="/ecommerce/grassbackground.png" alt="Grass Background Banner" class="w-full" />
	<div class="flex items-center justify-between text-xl">
		<span>BACK TO CART</span>
		<span>VINLYZ.NET</span>
	</div>
	<section class="flex gap-4 w-full">
		<div class="w-3/5 rounded-md flex items-center justify-center gap-8 border border-black">
			{#each [1, 2, 3] as i}
				<div class="relative">
					<img src="/ecommerce/cd{i}.png" alt={"CD " + i} />
					<div
						class="absolute bg-white right-0 top-0 w-8 h-8 flex items-center
            justify-center border border-black rounded-full"
					>
						x1
					</div>
				</div>
			{/each}
		</div>
		<div class="w-2/5 px-6 py-2 rounded-md border border-black">
			<h2>SHOPPING CART</h2>
			{#each shoppingCart as item}
				<ol>
					<li class="text-sm flex gap-10 items-center justify-between">
						<span>{item.title}</span>
						<span>...${item.price}</span>
					</li>
				</ol>
			{/each}
		</div>
	</section>
	<section class="grid grid-cols-2 gap-4">
		<div class="rounded-md border flex border-black p-4">
			<div class="text-sm w-1/2 flex flex-col gap-8">
				<h3>PAYMENT METHOD</h3>
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
				<button>MAKE SOME CHANGES</button>
			</div>
			<div class="flex flex-col gap-8">
				<div>
					<label for="card-number">CARD NUMBER</label>
					<input name="card-number" class="p-2 w-full border border-black rounded-lg" />
				</div>
				<div>
					<label for="card-name">NAME ON CARD</label>
					<input name="card-name" class="p-2 w-full border border-black rounded-lg" />
				</div>
				<div>
					<label for="expiration">EXPIRATION DATE</label>
					<input name="expiration" class="p-2 w-full border border-black rounded-lg" />
				</div>
				<div>
					<label for="cvv">CVV</label>
					<input name="cvv" class="p-2 w-full border border-black rounded-lg" />
				</div>
			</div>
		</div>
		<div>
			<img src="/ecommerce/promo.png" alt="Promo Banner" class="w-full" />
		</div>
	</section>
</main>
