<script>
	export let submission;
</script>

<a
	href="/day{submission.day}"
	class="group relative flex h-full cursor-pointer flex-col gap-4 rounded-lg bg-[#fc7373] bg-opacity-60 p-4 pt-8 transition hover:bg-opacity-100"
>
	<img
		src="/diagonalarrow.svg"
		alt="Link Icon"
		class="absolute right-2 top-2 transition-transform group-hover:-translate-y-1 group-hover:translate-x-1"
	/>
	<img src="/submissions/day{submission.day}.png" alt="Submission Screenshot" />
	<span class="max-w-max rounded-full bg-[#ffdada] px-2 py-1 text-sm font-bold text-[#fc7373]"
		>Day {submission.day}</span
	>
	<p class="leading-6">
		<span class="font-bold">{submission.title}</span>
		<span class="text-sm">by @{submission.username}</span>
	</p>
</a>
