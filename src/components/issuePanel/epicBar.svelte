

<script>
    import {Sidebar,
		SidebarGroup,
		SidebarItem} from 'flowbite-svelte';
	let spanClass = 'flex-1 ms-3 whitespace-nowrap';
	let activeClass = 'flex bg-primary-700 rounded-lg text-white hover:bg-gray-700';
	let nonActiveClass = 'flex p-2  hover:bg-green-700';


    export let epic = Array();

</script>
<Sidebar {activeClass} {nonActiveClass} class="bg-gray-700">
    <SidebarGroup>

        {#each epic as {name}}
        <SidebarItem class="font-bold" style="color: #ffffff;" label={name}></SidebarItem>
        {/each}
       
    </SidebarGroup>
</Sidebar>


<!--  <SidebarItem class="font-bold" style="color: #ffffff;" label="Dashboard"></SidebarItem>

        <SidebarItem class="font-bold" style="color: #ffffff;" label="Kanban" {spanClass}>
            <svelte:fragment slot="subtext">
                <span
                    class="ms-3 inline-flex items-center justify-center rounded-full bg-gray-200 px-2 text-sm font-medium text-gray-800 dark:bg-gray-700 dark:text-gray-300"
                >
                    Pro
                </span>
            </svelte:fragment>
        </SidebarItem>
     <SidebarItem label="Inbox" {spanClass}>
                <svelte:fragment slot="subtext">
                    <span
                        class="ms-3 inline-flex h-3 w-3 items-center justify-center rounded-full bg-primary-200 p-3 text-sm font-medium text-primary-600 dark:bg-primary-900 dark:text-primary-200"
                    >
                        3
                    </span>
                </svelte:fragment>
            </SidebarItem> 
            <SidebarItem class="font-bold" style="color: #ffffff;" label="Users"></SidebarItem>
            <SidebarItem class="font-bold" style="color: #ffffff;" label="Products"></SidebarItem>
            <SidebarItem class="font-bold" style="color: #ffffff;" label="Sign In"></SidebarItem>
            <SidebarItem class="font-bold" style="color: #ffffff;" label="Sign Up"></SidebarItem> -->