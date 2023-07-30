<script>
  import "../app.postcss";
  import cyberxlg from "$lib/img/cyberxlogo.png"
  import { DarkMode } from 'flowbite-svelte';
  import { Navbar, NavBrand, NavLi, NavUl, NavHamburger } from 'flowbite-svelte';
  import { Footer, FooterCopyright, FooterLinkGroup, FooterLink } from 'flowbite-svelte';
</script>

<Navbar let:hidden let:toggle rounded color="form">
  <NavBrand href="/">
    <img src={cyberxlg} class="mr-3 h-6 sm:h-9" alt="Logo"/>
    <span class="self-center whitespace-nowrap text-xl font-semibold dark:text-white">Cyber X</span>
  </NavBrand>
  <NavHamburger on:click={toggle} />
  <NavUl {hidden}>
    <NavLi href="/" active={true}>Home</NavLi>
    <NavLi href="/about">About</NavLi>
    <NavLi href="/services">Services</NavLi>
    <NavLi href="/pricing">Pricing</NavLi>
    <NavLi href="/contact">Contact</NavLi>
  </NavUl>
</Navbar>

<div class="flex justify-end m-2">
  <DarkMode />
</div>



<slot />

<Footer>
  <FooterCopyright href="https://dajix.vercel.app/" by="d3j1x" year={2023} />
  <FooterLinkGroup ulClass="flex flex-wrap items-center mt-3 text-sm text-gray-500 dark:text-gray-400 sm:mt-0">
    <FooterLink href="/">About</FooterLink>
    <FooterLink href="/">Privacy Policy</FooterLink>
    <FooterLink href="/">Licensing</FooterLink>
    <FooterLink href="/">Contact</FooterLink>
  </FooterLinkGroup>
</Footer>