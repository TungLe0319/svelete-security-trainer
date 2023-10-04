<!-- index.svelte -->
<script>
  // Your Svelte script logic here (if needed)
  import Flashcard from "../Components/flashcard.svelte";
</script>

<!-- Style using Tailwind CSS classes -->
<style>
  /* Apply global styles to the body */
  body {
    background-color: #0a2540; 
    @apply h-screen;
  }

  /* Style the container with a blue/white glow on hover */
  .container {
    @apply mx-auto max-w-screen-md p-4;
    background-color: #0077b6; /* Blue background color */
    border-radius: 8px; /* Rounded corners */
    box-shadow: 0 0 10px rgba(255, 255, 255, 0.5); /* White glow on hover */
    transition: box-shadow 0.3s ease-in-out;
  }

  .container:hover {
    box-shadow: 0 0 20px rgba(255, 255, 255, 0.7); /* Increase glow on hover */
  }

  /* Style the title */
  h1 {
    font-size: 2rem;
    color: white; /* White text color */
  }

  /* Style the link */
  a {
    color: #ffb400; /* Yellow link color */
  }

  /* Remove underline from links */
  a:hover {
    text-decoration: none;
  }
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
