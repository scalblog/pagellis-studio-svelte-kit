<script>
  import { onMount } from 'svelte';
  import { page } from '$app/stores';

  let isMenuOpen = false;
  let scrollY;

  function toggleMenu() {
    isMenuOpen = !isMenuOpen;
  }

  onMount(() => {
    const unsubscribe = page.subscribe(() => {
      isMenuOpen = false;
    });

    return () => {
      unsubscribe();
    };
  });
</script>

<svelte:window bind:scrollY />

<header class:scrolled={scrollY > 50} class="fixed w-full z-50 transition-all duration-300">
  <div class="container mx-auto px-4 py-4 flex justify-between items-center">
    <a href="/" class="text-2xl font-bold text-gray-800">Pagellis Studio</a>
    
    <nav class="hidden md:flex space-x-6">
      <a href="/" class="text-gray-600 hover:text-gray-800">Home</a>
      <a href="/services" class="text-gray-600 hover:text-gray-800">Services</a>
      <a href="/a-propos" class="text-gray-600 hover:text-gray-800">About</a>
      <a href="/contact" class="text-gray-600 hover:text-gray-800">Contact</a>
    </nav>

    <button on:click={toggleMenu} class="md:hidden">
      <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16m-7 6h7"></path>
      </svg>
    </button>
  </div>

  {#if isMenuOpen}
    <div class="md:hidden bg-white">
      <nav class="container mx-auto px-4 py-4 flex flex-col space-y-4">
        <a href="/" class="text-gray-600 hover:text-gray-800">Home</a>
        <a href="/services" class="text-gray-600 hover:text-gray-800">Services</a>
        <a href="/a-propos" class="text-gray-600 hover:text-gray-800">About</a>
        <a href="/contact" class="text-gray-600 hover:text-gray-800">Contact</a>
      </nav>
    </div>
  {/if}
</header>

<style>
  header {
    background-color: rgba(255, 255, 255, 0.9);
    backdrop-filter: blur(5px);
  }

  header.scrolled {
    box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
  }
</style>
