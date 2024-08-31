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
</style>
