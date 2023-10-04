<!-- index.svelte -->
<script>
  // Your Svelte script logic here (if needed)
  import Flashcard from "../Components/flashcard.svelte";
</script>

<!-- Style using Tailwind CSS classes -->
<style>

</style>

<!-- HTML structure -->
<body>
  <!-- Container for the title with blue/white glow on hover -->
  <div class="container ">
    <h1 class="  justify-center flex">Welcome to Security Training</h1>
  
  </div>

 
  <div class=" flex justify-center p-4 m-4">
    <Flashcard />
  </div>
</body>
