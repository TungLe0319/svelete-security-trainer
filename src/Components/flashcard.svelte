<script>
  let isFlipped = false;
  let showPopup = false;
  
  // Flashcard data
  let term = "Security Term";
  let answer = "Security Answer";
  
  // Function to flip the card
  function flipCard() {
    isFlipped = !isFlipped;
  }
  
  // Function to show the confirmation popup
  function showConfirmationPopup() {
    showPopup = true;
  }
  
  // Function to close the confirmation popup
  function closePopup() {
    showPopup = false;
  }
</script>

<div class="flashcard" class:flipped={isFlipped}>
  <div class="card-front" on:click={flipCard}>
    {term}
  </div>
  <div class="card-back" on:click={flipCard}>
    {answer}
  </div>
  {#if showPopup}
    <div class="confirmation-popup">
      <p>Are you sure you want to reveal the answer?</p>
      <button on:click={flipCard}>Yes</button>
      <button on:click={closePopup}>No</button>
    </div>
  {/if}
</div>

<style>
  /* Add your CSS styles here */
  .flashcard {
    width: 200px;
    height: 300px;
    perspective: 1000px;
  }
  
  .card-front,
  .card-back {
    width: 100%;
    height: 100%;
    display: flex;
    justify-content: center;
    align-items: center;
    font-size: 1.5rem;
    background-color: #f5f5f5;
    border: 1px solid #ccc;
    border-radius: 5px;
    position: absolute;
    backface-visibility: hidden;
    transition: transform 0.5s;
  }
  
  .card-front {
    transform: rotateY(0deg);
  }
  
  .card-back {
    transform: rotateY(180deg);
  }
  
  .flipped .card-front {
    transform: rotateY(180deg);
  }
  
  .flipped .card-back {
    transform: rotateY(0deg);
  }
  
  .confirmation-popup {
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    background-color: white;
    padding: 20px;
    border: 1px solid #ccc;
    box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
  }
</style>
