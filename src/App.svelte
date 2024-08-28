<script>
   let Name = "Youcef";
   let NickName = "Mantas";
   $: fullName = `${Name} ${NickName}`;
   $: {
      console.log(Name);
      console.log(NickName);

   }
   const handleClick = () =>{
      Name = NickName;
   }
   const handleChange = (e) =>{
      Name = e.target.value;
   }
   </script>
   
   <main>
    <div class="container">
      <h1>Hello {fullName}</h1>
      <button on:click={handleClick} style="color: {Name};">Click</button>
      <span>By Clicking On Button You Will Know NickName!</span>
      <input type="text" bind:value={Name} >
      <input type="text" bind:value={NickName} >


    </div>     
   </main>
   
   <style>
      .container {
          display: flex;
          flex-direction: column;
          align-items: center;
      }
   
      h1, button, span, input {
          margin: 0.5rem 0; /* Adds some space between the elements */
      }
      span {
          color: antiquewhite;
      }
   </style>
   