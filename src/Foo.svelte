<script>
    export let message = "default Value";
    let Foo = true;
    let isModal = true;
</script>
<main>
    {#if Foo}
    <div class="backdrop">
      <div class="first-class" class:Modal={isModal}>
       <p><strong>{message}</strong></p>
      </div>
    </div>
    {/if}
</main>
<style>
    .first-class {
        background-color: antiquewhite;
    }
    p {
        color: deepskyblue;
        font-family: monospace;
        font-size: large;
    }
    .Modal {
        background-color: crimson;
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
