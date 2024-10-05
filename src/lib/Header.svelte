<script>
  import Hamburger from '$lib/Hamburger.svelte';
  export let open = false;
</script>

<header class="flex justify-between bg-gray-200 p-2 items-center text-gray-600 border-b-2">
	<nav class="flex">
    <a href="/" class="text-gray-600 hover:text-gray-800">Home</a>
    <a href="/" class="text-gray-600 hover:text-gray-800 ml-4">About</a>
    <Hamburger bind:open={open}/>
	</nav>
</header>

<style>
  header {
    position: fixed;
    width: 100%;
    z-index: 10;
    justify-content: right;
  }
</style>