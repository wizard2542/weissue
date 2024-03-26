<script>
	import {
		AccordionItem,
		Accordion,
		Sidebar,
		SidebarDropdownItem,
		SidebarDropdownWrapper,
		SidebarGroup,
		SidebarItem,
		SidebarWrapper,
		Gallery
	} from 'flowbite-svelte';

	const items = Array(3);
	let spanClass = 'flex-1 ms-3 whitespace-nowrap';

  let activeClass = 'flex items-center p-2 text-base font-normal bg-primary-700 rounded-lg text-white hover:bg-gray-700';
  let nonActiveClass = 'flex items-center p-2 text-base font-normal rounded-lg hover:bg-green-700';
  
	const open_all = () => items.forEach((_, i) => (items[i] = true));
	const close_all = () => items.forEach((_, i) => (items[i] = false));

	import SubCard from './subCard.svelte';
</script>

<!-- <Button on:click={open_all}>Open all</Button>
<Button on:click={close_all}>Close all</Button> -->
<Gallery class="grid grid-cols-6 " >
	<Sidebar {activeClass} {nonActiveClass} class="bg-gray-700">
			<SidebarGroup >
				<SidebarItem class="font-bold" style="color: #ffffff;" label="Dashboard"></SidebarItem>
				
				<SidebarItem class="font-bold" style="color: #ffffff;" label="Kanban" {spanClass}>
					<svelte:fragment slot="subtext">
						<span
							class="ms-3 inline-flex items-center justify-center rounded-full bg-gray-200 px-2 text-sm font-medium text-gray-800 dark:bg-gray-700 dark:text-gray-300"
						>
							Pro
						</span>
					</svelte:fragment>
				</SidebarItem>
				<!-- <SidebarItem label="Inbox" {spanClass}>
					<svelte:fragment slot="subtext">
						<span
							class="ms-3 inline-flex h-3 w-3 items-center justify-center rounded-full bg-primary-200 p-3 text-sm font-medium text-primary-600 dark:bg-primary-900 dark:text-primary-200"
						>
							3
						</span>
					</svelte:fragment>
				</SidebarItem> -->
				<SidebarItem class="font-bold" style="color: #ffffff;" label="Users"></SidebarItem>
				<SidebarItem class="font-bold" style="color: #ffffff;" label="Products"></SidebarItem>
				<SidebarItem class="font-bold" style="color: #ffffff;" label="Sign In"></SidebarItem>
				<SidebarItem class="font-bold" style="color: #ffffff;" label="Sign Up"></SidebarItem>
			</SidebarGroup>
	</Sidebar>

	<Accordion multiple shadow="true" class="col-span-5" activeClass="bg-primary-600 text-white focus:ring-4 focus:ring-blue-800" inactiveClass="text-white hover:bg-white hover:text-gray-800">
		<AccordionItem bind:open={items[4]}>
			<span slot="header"><b>Change Main</b></span>
			<p class="m-2" style="color: #ffffff;">
				<b>
					Lorem ipsum dolor sit amet, consectetur adipisicing elit. Illo ab necessitatibus sint
					explicabo ...
				</b>
			</p>
			<SubCard></SubCard>
		</AccordionItem>
		
	</Accordion>
</Gallery>
