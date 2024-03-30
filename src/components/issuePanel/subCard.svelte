<script>
	import {
		AccordionItem,
		Accordion,
		Textarea,
		Card,
		Gallery,GradientButton
	} from 'flowbite-svelte';
	import { CodeOutline } from 'flowbite-svelte-icons';
	const items = Array(3);
	const open_all = () => items.forEach((_, i) => (items[i] = true));
	const close_all = () => items.forEach((_, i) => (items[i] = false));

    export let name='';
    export let des='';
    export let req;
    export let res;
    export let index;
</script>



<Accordion multiple shadow="true" rounded="true" border="true" activeClass="bg-white text-gray-800 focus:ring-4 focus:ring-blue-800" inactiveClass="text-gray-800 bg-white hover:bg-primary-600 hover:text-white" >
    <AccordionItem bind:open={items[6]} >
        <span slot="header" class=" font-bold">Issue {index} : {name}</span>
        <p class="m-4 font-bold " style="color: #ffffff;">
           {des}
        </p>
        <Gallery  class="gap-4 grid-cols-1 md:grid-cols-2 font-bold m-4">
            <Card shadow="true" color="orange" size='lg' style="background-color: #ffb1a5;">
                <Gallery class="grid-cols-3 mb-2">
                    <h5 class=" text-2xl tracking-tight">
                        Request
                    </h5>
                    <div></div>

                    <GradientButton   shadow="pink" color="pinkToOrange" name="Format code"><CodeOutline /></GradientButton>
                </Gallery>

                <Gallery class="gap-4 grid-cols-1">
                    <Textarea id="textarea-id" placeholder="Your message" rows="8" name="message" />
                </Gallery>
            </Card>
            <Card shadow="true" size='lg' style="background-color: #42b883; color: #000000">

                <Gallery class="grid-cols-3 mb-2">
                    <h5 class=" text-2xl tracking-tight">
                        Response
                    </h5>
                    <div></div>

                    <GradientButton   shadow="pink" color="pinkToOrange" name="Format code"><CodeOutline /></GradientButton>
                </Gallery>

                <Gallery class="gap-4 grid-cols-1">
                    <Textarea id="textarea-id" placeholder="Your message" rows="8" name="message" />
                </Gallery>

            </Card>
        </Gallery>
    </AccordionItem>

</Accordion>