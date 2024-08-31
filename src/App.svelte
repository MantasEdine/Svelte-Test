<script>
   import Foo from "./Foo.svelte";
 let people = [
    { name: 'John', surname : 'Michael', age: 25, id : 1 },
    { name: 'Karl', surname : 'Max', age: 26, id : 2 },
    { name: 'Joseph', surname : 'Stalin', age: 27, id : 3 },

]  
    
    const handleDelete = (id) =>{
      people = people.filter(person =>{
       return  person.id != id;
      })
     
    }
   
   </script>
   
<Foo/>
   <main>
    {#if people.length >= 3}
     <div class="container">
      <h1>People Infos :</h1>
      {#each people as person (person.id) }
      <h4>{person.name}</h4>
      <span>{person.surname}</span>
      <span>{person.age}</span>
      <button on:click={()=> handleDelete(person.id)}>delete</button>
      {:else}
      <p>No people found</p>
      {/each}
      
      
     </div>   
     {:else}  
     <p>So Sad</p>
     {/if}
   </main>
   
   <style>
      .container {
          display: flex;
          flex-direction: column;
          align-items: center;
      }
   
      h1 {
          margin: 0.5rem 0; /* Adds some space between the elements */
      }
      span {
          color: antiquewhite;
      }
   </style>
   