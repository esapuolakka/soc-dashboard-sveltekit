<svelte:head>
	<link href="https://unpkg.com/tailwindcss@^1.0/dist/tailwind.min.css" rel="stylesheet"/>
</svelte:head>


<script>
  import Header from "$lib/Header.svelte";
  import Sidebar from "$lib/Sidebar.svelte";
  let open = false;
</script>

<Header bind:open={open}/>
<Sidebar bind:open={open} />

<main>
  <slot />
</main>

<footer></footer>

<style>
  @import url("https://fonts.googleapis.com/css2?family=Kanit:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,100;1,200;1,300;1,400;1,500;1,600;1,700;1,800;1,900&display=swap");

  :root {
    --primary-color: #2c3e50;
    --secondary-color: #34495e;
    --accent-color: #e74c3c;
    --light-color: #ecf0f1;
    --dark-color: #2c3e50;
    --primary-font: "Kanit", sans-serif;
    --nav-font-weight: 300;
    --nav-font-size: 1rem;
    --dark-bg-color: #rgb(48, 49, 63);
    --sidebar-bg-color: #f7fafb;
  }
</style>
