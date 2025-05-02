<script>
	
	// @ts-ignore
	import Carousel from 'svelte-carousel';
	import { browser } from '$app/environment';

	const opinions = [
		{
			usr: 'dillfrescott',
			img: '/opinion-1.jpg',
			msg: 'Just discovered this today. this is one of those projects that stands out for me as really neat. Keep up the good work!'
		},
		{
			usr: 'Eliyaan',
			img: '/opinion-2.jpg',
			msg: 'I tested it in the browser with a friend, it works very well. Thanks for your work!'
		}
	];
	
</script>

{#if browser}

		{#each opinions as { img, msg, usr }}
			<ul class="pt-10 pb-10 w-fit px-10">
				<!-- Chat -->
				<li class="max-w-lg flex">
					<img class="inline-block size-9 rounded-full me-2" src={img} alt={`Avatar ${usr}`} />
					<!-- Card -->
					<div
						class="rounded-2xl p-4 space-y-3 bg-neutral-900 shadow-2xl border-neutral-700 border-2"
					>
						<div class="space-y-1.5">
							<p class="mb-1.5 text-sm text-white">
								{msg}
							</p>
						</div>
					</div>
					<!-- End Card -->
				</li>
				<!-- End Chat -->
			</ul>
		{/each}
{/if}
