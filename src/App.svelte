<script>
let colour = "gold"
let defaultColour = "Black";
   
   const handleClick = () =>{
    colour = defaultColour;
   }
   const handleInput = (event) =>{
   colour = event.target.value;
   }
</script>

<main>
   
   <h1 style="color: {colour};">Hello <strong>{colour}</strong></h1>
   <button on:click={handleClick}>Click Me)</button>
   <!--Two Way Data Binding-->
   <!-- <input type="text" on:change={handleInput} value={colour}> -->
   <input type="text" bind:value={colour}>
     
</main>

<style>
 
</style>
