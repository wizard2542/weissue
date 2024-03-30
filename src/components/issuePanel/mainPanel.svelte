<script>
	import { Gallery } from 'flowbite-svelte';
	import TopicCard from './topicCard.svelte';
	import EpicBar from './epicBar.svelte';

	const open_all = () => items.forEach((_, i) => (items[i] = true));
	const close_all = () => items.forEach((_, i) => (items[i] = false));

	let data = {
		epic: [
			{
				name: 'HBlot_1',
				topic: [
					{
						name: 'Change Main',
						des: 'Change Main Support Add new Main promotion and also Delete old Main promotion',
						issues: [
							{
								name: 'Add 2 Main ',
								des: '',
								req: '',
								res: ''
							},
							{
								name: 'Add Main Delete Ontop',
								des: '',
								req: '',
								res: ''
							},
							{
								name: 'Add Main Delete Ontop Extra',
								des: '',
								req: '',
								res: ''
							}
						]
					},
					{
						name: 'Change Ontop',
						des: 'Change Ontop Support Add new Ontop promotion and also Delete old Ontop promotion'
					}
				]
			},
			{
				name: 'HBlot_2',
				topic: [
					{
						name: 'PayOnSpot',
						des: 'Change Main Support Add new Main promotion and also Delete old Main promotion',
						issues: [
							{
								name: 'Add 2 Main ',
								des: '',
								req: '',
								res: ''
							},
							{
								name: 'Add Main Delete Ontop',
								des: '',
								req: '',
								res: ''
							},
							{
								name: 'Add Main Delete Ontop Extra',
								des: '',
								req: '',
								res: ''
							}
						]
					},
					{
						name: 'Change GSM HandSet',
						des: 'Change Ontop Support Add new Ontop promotion and also Delete old Ontop promotion'
					}
				]
			}
		]
	};
</script>

<!-- <Button on:click={open_all}>Open all</Button>
<Button on:click={close_all}>Close all</Button> -->
<Gallery class="grid grid-cols-6 ">
	<EpicBar epic={data.epic} />

	<div class="col-span-5">
		{#each data.epic[0].topic as subCard, i}
			<TopicCard {...subCard} />
		{/each}
	</div>
</Gallery>
