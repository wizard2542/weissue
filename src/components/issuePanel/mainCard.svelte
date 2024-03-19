<script>
	import {
		AccordionItem,
		Accordion,
		Button,
		Textarea,
		Card,
		Toolbar,
		ToolbarGroup,
		ToolbarButton,
		Gallery
	} from 'flowbite-svelte';
	import { ArrowRightOutline } from 'flowbite-svelte-icons';
	import { CodeOutline, FaceGrinOutline } from 'flowbite-svelte-icons';
	const items = Array(3);
	const open_all = () => items.forEach((_, i) => (items[i] = true));
	const close_all = () => items.forEach((_, i) => (items[i] = false));
</script>

<!-- <Button on:click={open_all}>Open all</Button>
<Button on:click={close_all}>Close all</Button> -->
<Accordion multiple>
	<AccordionItem bind:open={items[0]} color="pink">
		<span slot="header">HB Lot 1 </span>

		<p class="mb-2 text-gray-500 dark:text-gray-400">
			Lorem ipsum dolor sit amet, consectetur adipisicing elit. Illo ab necessitatibus sint
			explicabo ...
		</p>

		<Accordion multiple>
			<AccordionItem bind:open={items[4]}>
				<span slot="header">Change Main</span>
				<p class="mb-2 text-gray-500 dark:text-gray-400">
					Lorem ipsum dolor sit amet, consectetur adipisicing elit. Illo ab necessitatibus sint
					explicabo ...
				</p>

				<Accordion multiple>
					<AccordionItem bind:open={items[6]}>
						<span slot="header">Issue 1</span>
						<p class="mb-2 text-gray-500 dark:text-gray-400">
							Lorem ipsum dolor sit amet, consectetur adipisicing elit. Illo ab necessitatibus sint
							explicabo ...
						</p>
						<Gallery class="gap-4 grid-cols-2 ">
							<Card>
								<Gallery class="grid-cols-2">
									<h5 class="mb-2 text-2xl font-bold tracking-tight text-gray-900 dark:text-white">
										Request
									</h5>

									<ToolbarButton color="indigo" name="Format code"><CodeOutline /></ToolbarButton>
								</Gallery>

								<Gallery class="gap-4 grid-cols-1">
									<Textarea id="textarea-id" placeholder="Your message" rows="8" name="message" />
								</Gallery>
							</Card>

							<Card>
								<Gallery class="grid-cols-2">
									<h5 class="mb-2 text-2xl font-bold tracking-tight text-gray-900 dark:text-white">
										Response
									</h5>

									<ToolbarButton color="indigo" name="Format code"><CodeOutline /></ToolbarButton>
								</Gallery>

								<Gallery class="gap-4 grid-cols-1">
									<Textarea id="textarea-id" placeholder="Your message" rows="8" name="message" />
								</Gallery>
							</Card>
						</Gallery>
					</AccordionItem>
					<AccordionItem bind:open={items[7]}>
						<span slot="header">Issue 2</span>
						<p class="mb-2 text-gray-500 dark:text-gray-400">
							Lorem ipsum dolor sit amet, consectetur adipisicing elit. Illo ab necessitatibus sint
							explicabo ...
						</p>
					</AccordionItem>
				</Accordion>
			</AccordionItem>
			<AccordionItem bind:open={items[5]}>
				<span slot="header">IR IDD RUC</span>
				<p class="mb-2 text-gray-500 dark:text-gray-400">
					Lorem ipsum dolor sit amet, consectetur adipisicing elit. Illo ab necessitatibus sint
					explicabo ...
				</p>
			</AccordionItem>
		</Accordion>
	</AccordionItem>

	<AccordionItem bind:open={items[1]}>
		<div slot="header">My Header 2</div>
		<p class="mb-2 text-gray-500 dark:text-gray-400">
			Lorem ipsum dolor sit amet, consectetur adipisicing elit. Illo ab necessitatibus sint
			explicabo ...
		</p>
		<p class="mb-2 text-gray-500 dark:text-gray-400">
			Lorem ipsum dolor sit amet, consectetur adipisicing elit. Illo ab necessitatibus sint
			explicabo ...
		</p>
		<p class="mb-2 text-gray-500 dark:text-gray-400">Learn more about these technologies:</p>
	</AccordionItem>

	<AccordionItem bind:open={items[2]}>
		<div slot="header">My Header 3</div>
		<p>Something more</p>
	</AccordionItem>
</Accordion>
