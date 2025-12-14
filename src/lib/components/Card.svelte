<script lang="ts">
	export let title: string;
	export let description: string | undefined = undefined;
	export let shadow: boolean = true;
	export let expand: boolean = false;
	export let icon: string = "";
</script>


	<article
		class="bg-white rounded-lg shadow-lg p-6 hover:bg-neutral group transition-colors duration-300 flex flex-col items-center"
		class:drop-shadow={shadow}
		class:w-full={expand}
		class:h-full={expand}
		class:py-auto={expand}
		class:px-auto={expand}
	>
	    {#if icon !== ""}
			{@html icon}
		{/if}
		<h2
			class="font-bold text-neutral group-hover:text-white transition-colors duration-300"
			class:text-2xl={description === undefined}
			class:text-center={description === undefined}
			class:text-lg={description !== undefined}
		>
			{title}
		</h2>
		{#if description}
			<p class="text-gray-600 group-hover:text-gray-400 transition-colors duration-300">
				{@html description}
			</p>
		{/if}
	</article>
