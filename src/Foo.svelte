<script>
    let Foo = true;
</script>
<main>
    {#if Foo}
    <div class="backdrop">
      <div class="Modal">
       <p><strong>Foo is the real hero !</strong></p>
      </div>
    </div>
    {/if}
</main>
<style>
    p {
        color: deepskyblue;
        font-family: monospace;
        font-size: large;
    }
    .Modal {
        background-color: red;
        border-radius: 10px;
        margin: auto;
        padding: 1rem;
        box-shadow: 
        3px 3px 5px rgba(0, 0, 0, 0.2),
        6px 6px 10px rgba(0, 0, 0, 0.15),
        9px 9px 15px rgba(0, 0, 0, 0.1);

    }
    .Modal:hover {
        cursor: pointer;
    }

</style>
