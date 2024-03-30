<script>
	import { AccordionItem, Accordion } from 'flowbite-svelte';

	import SubCard from './subCard.svelte';

	export let name;
	export let des;
	export let issues = Array();
</script>

<!-- {#each issues as item } 
        
<SubCard {...item}></SubCard>

{/each} -->

<!-- <Accordion>
    <AccordionItem>
      <span slot="header" class="text-base flex gap-2">
        <span>My Header 1</span>
      </span>
      <p class="mb-2 text-gray-500 dark:text-gray-400">Lorem ipsum dolor sit amet, consectetur adipisicing elit. Illo ab necessitatibus sint explicabo...</p>
      <p class="text-gray-500 dark:text-gray-400">
        Check out this guide to learn how to <a href="/" target="_blank" rel="noreferrer" class="text-blue-600 dark:text-blue-500 hover:underline"> get started </a>
        and start websites even faster with components on top of Tailwind CSS.
      </p>
    </AccordionItem>
</Accordion> -->

<Accordion
	shadow="true"
	activeClass="bg-primary-600 text-white focus:ring-4 focus:ring-blue-800"
	inactiveClass="text-white hover:bg-white hover:text-gray-800"
>
	<AccordionItem>
		<span slot="header"><b>{name}</b></span>
		<p class="m-2" style="color: #ffffff;">
			<b>
				{des}
			</b>
		</p>

		{#if issues.length != 0}
			{#each issues as item, i}
				<SubCard {...item} index={i}></SubCard>
			{/each}
		{:else}
			<p style="color: red;"><b>Have not any Issue yet</b></p>
		{/if}
	</AccordionItem>
</Accordion>
