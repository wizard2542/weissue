<script>
    import { Navbar, NavBrand, NavLi, NavUl, NavHamburger } from 'flowbite-svelte';
    
  import { CalendarWeekSolid } from 'flowbite-svelte-icons';

  </script>
  
  <Navbar rounded color="form">
    <NavBrand href="/">
      <CalendarWeekSolid size="xl"/>
      
      <span class="self-center whitespace-nowrap text-xl font-semibold dark:text-white">WeIssue</span>
    </NavBrand>
    <NavHamburger />
    <NavUl>
      <NavLi href="/" active={true}>Home</NavLi>
      <NavLi href="/about">About</NavLi>
      <NavLi href="/docs/components/navbar">Navbar</NavLi>
      <NavLi href="/pricing">Pricing</NavLi>
      <NavLi href="/contact">Contact</NavLi>
    </NavUl>
  </Navbar>